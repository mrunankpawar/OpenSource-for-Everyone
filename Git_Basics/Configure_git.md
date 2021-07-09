# Configure Git
We want to configure our local environments so that the correct GitHub account is associated with our commits. 

- On GitHub, find your user name. You can find it by clicking your avatar in the upper right hand corner. It will say "Signed in as"
- Return to your command line or terminal. Replace `user_name` with your username. 
  - ```git config --global user.name "user_name"```
- Use the command below to configure your email address as well. 
  - ```git config --global user.email "my_email_id@domain.com"```
- You can use the two commands below to double check that you've set this up.  
```
@PulkitSingh > git config user.name
>>> user_name
@PulkitSingh > git config user.email
>>> my_email_id@domain.com
```

**Now, let's cover some useful commands.**
