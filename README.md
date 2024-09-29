# Git-Github

Author: Nihar Muniraju


Connecting Remote GitHub Repository to Local Git and Pushing Changes: Detailed Guide

Step 1: Install Git on Your Local Machine
Before you can start using Git, you need to install it on your machine.

For macOS: `brew install git`

For Ubuntu/Linux: `sudo apt-get update` and `sudo apt-get install git`

For Windows: Download the Git installer from the official website and follow the instructions.
Once installed, verify the installation with `git --version`.

Diagram: Local Git Repository <--------> Remote GitHub Repository
Step 2: Configure Git
After installing Git, configure your username and email:

1. `git config --global user.name 'Your Name'`
2. `git config --global user.email 'your.email@example.com'`

This associates your commits with your identity.
Step 3: Create a New Repository on GitHub
Go to GitHub, log in, and create a new repository:

1. Click on 'New' to create a repository.
2. Provide a name and description.
3. Do not initialize the repository with a README if you have existing code.

Diagram: GitHub New Repository Creation.
Step 4: Initialize Git in Your Local Directory
Navigate to your project folder and initialize Git:

1. `cd /path/to/your/project`
2. `git init`

This creates a .git folder in your directory, marking it as a Git repository.
Step 5: Connect Local Repository to Remote GitHub Repository
Connect your local repository to the remote GitHub repository:

1. Add the GitHub remote: `git remote add origin https://github.com/yourusername/your-repo-name.git`
2. Verify the remote: `git remote -v`

Diagram: Local Repository connected to GitHub.
Step 6: Stage and Commit Your Changes
Stage your files:

`git add .`

Commit your changes:

`git commit -m 'Initial commit'`
Step 7: Push Local Repository to GitHub
Push your changes to GitHub:

`git push -u origin master` or `git push -u origin main`.
Step 8: Pulling Changes from the Remote Repository
Pull the changes from GitHub to your local repository:

`git pull origin master`
Step 9: Set up SSH Key for Password-less Authentication
Set up SSH key for authentication:

1. Generate SSH key: `ssh-keygen -t rsa -b 4096 -C 'your.email@example.com'`
2. Add the SSH key to GitHub under SSH and GPG keys.
3. Set the SSH URL for the repository: `git remote set-url origin git@github.com:yourusername/your-repo-name.git`
