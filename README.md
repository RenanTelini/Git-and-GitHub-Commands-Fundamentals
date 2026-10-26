# Git and GitHub Commands - Fundamentals

#### This exercise/repository is based on the <a href="https://www.udemy.com/course/programacao-orientada-a-objetos-csharp/?couponCode=MT260714G2">"C# COMPLETO Programação Orientada a Objetos + Projetos"</a> course.

#### This repository covers the use of Git commands to use the GitHub and your resources.

### <ins>Git and GitHub Commands</ins>

#### <ins>What is Git and GitHub?</ins>

#### - GitHub: GitHub is an online platform for hosting and managing Git repositories, enabling developers to store, share, and collaborate on projects.

#### - Git: Git is a version control system that allows you to track changes to files and projects over time. It stores a history of changes, enabling you to access previous versions, compare changes, and restore earlier states of your project, from its initial version to its latest version.


#### <ins>What Do You Need to Use Git and GitHub?</ins>

#### - Create a GitHub account. <a href="https://github.com">Sign up for an account on GitHub.</a> 

#### - Install Git. <a href="https://git-scm.com/install/windows">Download and install Git</a> from the official Git website. After installation, you can open Git Bash and run the following command to check whether Git was installed correctly:

`git --version`

#### If the installation was successful, the command will display the installed Git version.

#### <strong>Optional:</strong> <a href="https://code.visualstudio.com/download">Download and install Visual Studio Code.</a> You can use Git Bash within VS Code, which also has built-in Git integration. In addition to showing files that have not yet been tracked by Git, VS Code allows you to review changes between file versions. This is especially useful when you try to push a new commit but your local repository is out of sync with the remote repository, which can lead to merge conflicts.

#### <ins>Configure Git</ins>

#### After installing Git, use the following commands to configure it:

#### - To set your name, run: `git config --global user.name "Your Name"`.

#### - To set your email address, run: `git config --global user.email "your.email@example.com"`.

#### <ins>Configure an SSH Key</ins>

#### SSH is a protocol for secure data communication.

#### The basic idea is to register which computers are authorized to access GitHub on your behalf. Computers that are not authorized will not be able to access your repositories using that SSH key.

#### To set this up, you need to:

- #### Generate an SSH key on your computer.
- #### Add the SSH public key to your GitHub account.

#### You can access:

- <a href="https://docs.github.com/pt/authentication/connecting-to-github-with-ssh">More about SSH Key</a>

- <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys">Checking for existing SSH keys</a>

- <a href ="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent">Generating a new SSH key and adding it to the ssh-agent</a>

- <a href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account">Adding a new SSH key to your GitHub account</a>


#### <ins>Your First Project</ins>

#### Now that everything is ready, open Git Bash and run the following commands to push your first project to GitHub:

- #### To initialize an empty repository in your local directory, run: `git init`.

- #### To rename the current branch to main: `git branch -M main`

- #### To add a remote repository: `git remote add origin <url-from-remote-repository>`. Links your local repository to a remote repository on GitHub. The name origin is the default convention for the remote repository.

- #### To adds all new, modified, and deleted files in the current directory and its subdirectories to the staging area, preparing them for the next commit, run: `git add .`

- #### To creates a commit containing the staged changes, run: `git commit -m "Your commit message"`. The -m flag lets you provide a message describing the changes.

- #### To push your changes to GitHub, run: `git push -u origin main`. Uploads your local main branch and its commits to the remote repository named origin. The -u flag sets the upstream branch, allowing you to use git push and git pull without specifying the remote and branch in future commands.