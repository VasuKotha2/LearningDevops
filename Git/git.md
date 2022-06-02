### Steps to create an SSH key for Github
-------------------------------------------
* Open terminal
* Paste the text below, substituting in your GitHub email address.
command to create an SSH key is `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
* This creates a new SSH key, using the provided email as a label.
 You will get a popup like this > Generating public/private algorithm key pair.
* Just press enter key till the SSH key gets generated.
* After that you can just cat the SSH key by navigating into the default location(.ssh/id_rsa.pub) and paste it in your Github account -> Settings -> SSH and GPG keys -> New SSH key

### Steps to create and delete a repository in github
-------------------------------------------------------
* To create a repository we can just click on new and give the repository name, description, select whether you want a public or private repository, if you want any readme.md file, add .gitignore file and choose a license  
* To delete a repository go to settings and 

* push an existing repository from the command line
    * `git remote add origin https://github.com/VasuKotha2/LearnigDevops.git` -> using https
    * `git remote add origin git@github.com:VasuKotha2/LearnigDevops.git` -> using SSH
    * `git branch -M main`
    * `git push -u origin main` -> to push the contents to your remote repository

* push an existing repository from the command line
    * `git remote add origin https://github.com/VasuKotha2/LearnigDevops.git` -> using https
    * `git remote add origin git@github.com:VasuKotha2/LearnigDevops.git` -> using SSH
    * `git branch -M main`
    * `git push -u origin main` -> to push the contents to your remote repository. Provide username and password.
* While pushing to the remote repository if you come accross an error like
    remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
    remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
    fatal: Authentication failed for 'https://github.com/VasuKotha2/LearningDevops.git/'

    This is because we need to generate a token to read/write contents from gihub.

### Creating a token in Github (Personal Access Token PAT)
------------------------------
* Go to settings -> Developer Settings -> Personal access tokens -> Generate new token -> Give your token a descriptive name -> select the Expiration drop-down menu, then click a default or use the calendar picker -> Select the scopes, or permissions, you'd like to grant this token -> Generate token