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

#### After that, you just need to go to your GitHub repository and refresh the page.

#### <ins>How To Create a New Commit</ins>

#### After sending the first version of your project to your GitHub repository, you can use these commands to create and send a new version of your project:”

#### `git status` - After making any changes to your project, use this command to check the changes.

#### `git add <file>` or `git add .` - After finishing your changes, use one of these commands to stage them. You can stage files individually using `git add <file>` or stage all changes at once using `git add .`.

#### <strong>Attention:</strong> Use the `git status` command to check whether you have staged any changes you didn't intend to include.

#### `git commit -m "Your commit message"` - You need to commit your changes every time you make any modifications to your project.

#### `git push` - To send your commits to your GitHub repository, use the `git push` command. You only need to use `git push -u origin main` the first time you push your project to the remote repository. After that, you can simply use `git push`.

#### By doing this, you will update your project in your GitHub repository with the latest version.

#### <ins>Some Other Git Commands:</ins>

#### `git clone <remote repository url>` - You can clone any public GitHub repository, but if you don't have permission to modify it, you won't be able to push your changes to the remote repository.

#### `git log` and `git log --oneline` - Use these commands to view your commit history.

- #### `git log` displays detailed information about each commit, including the commit hash, author, date, and commit message.

- #### `git log --oneline` displays a more concise version of the commit history, showing each commit's abbreviated hash and commit message on a single line.

#### <strong>Note:</strong> You can use these commands to see which commits exist in your local repository. However, they do not directly tell you whether your local branch is up to date with the remote repository. To check for differences between your local and remote branches, use `git fetch` followed by `git status`.

#### `git fetch` - This command downloads the latest commits, files, and references from a remote repository to your local repository, but it does not modify or merge these changes into your current working branch.

#### `git pull` - With this command, you download the latest updates from the remote repository, includding the commit history.

#### <strong>Attention:</strong> This command may cause merge conflicts if you and someone else have modified the same parts of a file in your local and remote branches. If this happens, you will need to resolve the conflicts before completing the merge.

#### `git status` - The `git status` command allows you to check the current state of your working directory and staging area. It displays information about changes in your project, including the following:

- Modified - When you modify a file in your project.
- Untracked - New files that Git is not tracking yet.
- Deleted - Files that have been deleted from your working directory.
- Staged - Changes that have been added to the staging area using `git add .` or `git add <file>`. These changes are ready to be included in the next commit.
- Committed - Changes that have been saved in a commit in your local repository.

#### `git diff` - "diff" stands for "difference". This command shows the changes in your working directory that have not yet been staged.

#### `git diff --staged` - Shows the differences between staged changes and the last commit.

#### `git checkout <commit hash>` or `git checkout HASH~1` - Temporarily switch to a specific commit or its parent commit, respectively.

#### <strong>Tip:</strong> Use "~1" to refer to the parent commit of the specified hash. To return to your current branch, run `git checkout <branch-name>`

#### <strong>Important:</strong> Before checking out to return to HEAD, make sure there are no uncommitted changes in your working directory. If you accidentally modified any files, discard the changes using:

- `git reset` - Removes changes from the staging area (index), effectively undoing the `git add` operation.

- `git clean -df` - Removes untracked files and directories from the working directory.

- `git checkout -- .` - Discards all local modifications to tracked files in the current directory and its subdirectories.

#### <strong>Tip:</strong> Always use `git status` before and after these operations to check the state of your working directory.

#### `git reset` - Removes modified files from the staging area.

#### `git restore <file>` - Discards local modifications to a specific file, restoring its content to the state recorded in the staging area (index).

#### `git restore .` - Discards local modifications to all tracked files in the current directory and its subdirectories.

#### `git restore --staged <file>` - The file is removed from the staging area, but its modifications are preserved in the working directory.

#### `git reset --soft HEAD~1` - Undoes the last commit while keeping all its changes in the staging area.

- Removes the last commit from the branch history.
- Preserves all file modifications.
- Keeps changes staged and ready for a new commit.

#### `git reset --hard <commit>` - Moves the current branch to the specified commit, discarding staged and unstaged changes in tracked files.

- Resets the branch history to the specified commit.
- Clears the staging area.
- Discards local modifications to tracked files.

#### <strong>Attention:</strong> This command can permanently delete uncommitted changes.

#### `git push -f` - Forces local commits to be pushed to the remote repository, overwriting the remote branch history when necessary.

- Updates the remote branch with the local history.
- Can overwrite existing commits in the remote repository.
- May cause other collaborators to lose their changes.

#### <strong>Attention:</strong> Use with caution, as it can overwrite other people's work.

#### `git remote -v` - Displays the remote repositories connected to your project and their URLs.

#### `git remote set-url origin <new url>` - Changes the URL of the remote repository named origin.

### <ins>VIM Editor</ins>

#### These actions may open the VIM editor in the terminal:

- Creating a commit without a message. - For example, when you run `git commit` and forget to include the `-m "<message commit>"` argument.
- Performing a three-way merge.

#### If this happens, follow these steps:

- Enter insert mode by pressing the "i" key on your keyboard.
- This enables text editing. Notice that "--INSERT--" appears in the bottom-left corner of the editor.

<img src="Imagens\VIM Editor.png">

- Type your commit message.
- To save your changes and exit the editor, press "Esc", type ":wq", and press "Enter".

<img src="Imagens/VIM Editor - !wq.png">

- To exit without saving your changes, press "Esc", type ":q!", and press "Enter".