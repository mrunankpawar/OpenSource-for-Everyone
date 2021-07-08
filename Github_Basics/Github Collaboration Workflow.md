# Developer Workflow
- You're going to practice a typical best practice developer workflow.
#

1. First, you'll fork someone else's code. This means creating your own copy of it.

2. Then you'll create a branch. The branch is a parallel version of your copy, where you'll test your own changes. 

3. You stage your changes as you go. When you're happy with them, you'll commit them. 

4. If you want to add your code to someone else's project, you'll open a pull request. 

5. If they approve it, they'll merge your branch into their master branch. 

- **Key Term:**
  - Fork: your own copy of someone else's repository. 
  - branch: a parallel version of the master copy of a repo. Making a branch allows you to edit code without accidentally breaking a working version.
  - stage: add to a cohesive group/bundle of revisions
  - commit: a group of revisions you want to officially add to your branch
  - merge:  to officially add the changes from your branch into the master branch (or another branch) 

**Great! That's it. That's how you work with Git. Let's try it using GitHub!**

# Network Activity Workflow
- As you can see, there are so many way to use GitHub! Today we're going to use a very common developer workflow. 
#

1. Fork the repository you want to contribute to or fork [this repository](https://github.com/PulkitSinghDev/OpenSource-for-Everyone)

![image](https://user-images.githubusercontent.com/71369943/124760720-a4c8d380-df4e-11eb-8679-f4deba2f9f03.png)

   - Note: This is only necessary if you are not a Collaborator on the project.  

2. Create a branch.  You should always try to name branches with your name and what you're doing, or follow the conventions set by your team. 

![image](https://user-images.githubusercontent.com/71369943/124761213-30426480-df4f-11eb-9478-f1f471881966.png)

3. Open [Documentation reviews.md](https://github.com/PulkitSinghDev/OpenSource-for-Everyone/blob/main/Documentation%20reviews.md)

![image](https://user-images.githubusercontent.com/71369943/124761471-77305a00-df4f-11eb-85f8-eed8e51aec08.png)

4. Select the edit icon. It looks like a pencil.

![image](https://user-images.githubusercontent.com/71369943/124761640-9e872700-df4f-11eb-9f71-ac4336ae1511.png)

5. Add the review accordingly as per the instructions given their

![image](https://user-images.githubusercontent.com/71369943/124762076-1c4b3280-df50-11eb-8348-16b834dc17f5.png)

6. Scroll to the bottom to the Commit changes section. 
7. Add a descriptive message. Select Commit changes.
8. Return to the main page of your repo.  
9. Select Pull request. 
10. Because this is a simple pull request, you can simply select Create Pull Request. If you were contributing to an open source project, you would want to be very descriptive about the changes you made. 
11. Ask someone else to comment on your PR. Comment on someone else's PR, too! You can find other pull requests by selecting the Pull requests tab on the repo's home page. 
12. This is what a pull request looks like for someone who has Write access to a repo. The organizer of this workshop will click Merge pull request, and your hometown will be added! 

## Conflict Resolution
- When a file has multiple edits, it can be unclear which change should be committed. This is a conflict and must be resolved before merging.
- A conflict is marked by 
```
<<<<<<< new branch
changes
=======
original
>>>>>>> original-branch
```
Edit the file to the desired state, mark it resolved and then merge it.

**Amazing! Now you know how to work with GitHub in the browser.**
