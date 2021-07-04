# Finding and customizing actions
Actions are the building blocks that power your workflow. A workflow can contain actions created by the community, or you can create your own actions directly within your application's repository. This guide will show you how to discover, use, and customize actions.

## Overview
The actions you use in your workflow can be defined in:

- A public repository
- The same repository where your workflow file references the action
- A published Docker container image on Docker Hub

GitHub Marketplace is a central location for you to find actions created by the GitHub community. GitHub Marketplace page enables you to filter for actions by category.

## Browsing Marketplace actions in the workflow editor
You can search and browse actions directly in your repository's workflow editor. From the sidebar, you can search for a specific action, view featured actions, and browse featured categories. You can also view the number of stars an action has received from the GitHub community.

1. In your repository, browse to the workflow file you want to edit.

![image](https://user-images.githubusercontent.com/71369943/124400787-cd7c7d80-dd42-11eb-8c93-f40f6a9012d2.png)

2. In the upper right corner of the file view, to open the workflow editor, click .

![image](https://user-images.githubusercontent.com/71369943/124400796-df5e2080-dd42-11eb-9d2f-f7f8a32737f7.png)

3. To the right of the editor, use the GitHub Marketplace sidebar to browse actions. Actions with the  badge indicate GitHub has verified the creator of the action as a partner organization.

![image](https://user-images.githubusercontent.com/71369943/124400825-087eb100-dd43-11eb-9d64-a9d2f41dce94.png)

## Adding an action to your workflow
An action's listing page includes the action's version and the workflow syntax required to use the action. To keep your workflow stable even when updates are made to an action, you can reference the version of the action to use by specifying the Git or Docker tag number in your workflow file.

Navigate to the action you want to use in your workflow.
Under "Installation", click  to copy the workflow syntax.
View action listing
Paste the syntax as a new step in your workflow. For more information, see "Workflow syntax for GitHub Actions."
If the action requires you to provide inputs, set them in your workflow. For information on inputs an action might require, see "Using inputs and outputs with an action."
You can also enable Dependabot version updates for the actions that you add to your workflow. For more information, see "Keeping your actions up to date with Dependabot."

Using release management for your custom actions
The creators of a community action have the option to use tags, branches, or SHA values to manage releases of the action. Similar to any dependency, you should indicate the version of the action you'd like to use based on your comfort with automatically accepting updates to the action.

You will designate the version of the action in your workflow file. Check the action's documentation for information on their approach to release management, and to see which tag, branch, or SHA value to use.

Note: We recommend that you use a SHA value when using third-party actions. For more information, see Security hardening for GitHub Actions

Using tags
Tags are useful for letting you decide when to switch between major and minor versions, but these are more ephemeral and can be moved or deleted by the maintainer. This example demonstrates how to target an action that's been tagged as v1.0.1:

steps:
  - uses: actions/javascript-action@v1.0.1
Using SHAs
If you need more reliable versioning, you should use the SHA value associated with the version of the action. SHAs are immutable and therefore more reliable than tags or branches. However this approach means you will not automatically receive updates for an action, including important bug fixes and security updates. You must use a commit's full SHA value, and not an abbreviated value. This example targets an action's SHA:

steps:
  - uses: actions/javascript-action@172239021f7ba04fe7327647b213799853a9eb89
Using branches
Specifying a target branch for the action means it will always run the version currently on that branch. This approach can create problems if an update to the branch includes breaking changes. This example targets a branch named @main:

steps:
  - uses: actions/javascript-action@main
For more information, see "Using release management for actions."

Using inputs and outputs with an action
An action often accepts or requires inputs and generates outputs that you can use. For example, an action might require you to specify a path to a file, the name of a label, or other data it will use as part of the action processing.

To see the inputs and outputs of an action, check the action.yml or action.yaml in the root directory of the repository.

In this example action.yml, the inputs keyword defines a required input called file-path, and includes a default value that will be used if none is specified. The outputs keyword defines an output called results-file, which tells you where to locate the results.

name: "Example"
description: "Receives file and generates output"
inputs:
  file-path: # id of input
    description: "Path to test script"
    required: true
    default: "test-file.js"
outputs:
  results-file: # id of output
    description: "Path to results file"
Referencing an action in the same repository where a workflow file uses the action
If an action is defined in the same repository where your workflow file uses the action, you can reference the action with either the ‌{owner}/{repo}@{ref} or ./path/to/dir syntax in your workflow file.

Example repository file structure:

|-- hello-world (repository)
|   |__ .github
|       └── workflows
|           └── my-first-workflow.yml
|       └── actions
|           |__ hello-world-action
|               └── action.yml
Example workflow file:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      # This step checks out a copy of your repository.
      - uses: actions/checkout@v2
      # This step references the directory that contains the action.
      - uses: ./.github/actions/hello-world-action
The action.yml file is used to provide metadata for the action. Learn about the content of this file in "Metadata syntax for GitHub Actions"

Referencing a container on Docker Hub
If an action is defined in a published Docker container image on Docker Hub, you must reference the action with the docker://{image}:{tag} syntax in your workflow file. To protect your code and data, we strongly recommend you verify the integrity of the Docker container image from Docker Hub before using it in your workflow.

jobs:
  my_first_job:
    steps:
      - name: My first step
        uses: docker://alpine:3.8
For some examples of Docker actions, see the Docker-image.yml workflow and "Creating a Docker container action."

Next steps
To continue learning about GitHub Actions, see "Essential features of GitHub Actions."
