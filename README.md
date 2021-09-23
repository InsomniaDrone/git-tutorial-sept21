# Getting started with git and github
This tutorial assumes that git has already been installed and the user has created an account on github. 

### 1. Open the terminal
- On a mac, type 'terminal' in spotlight (or iTerm2 if you prefer)
- On windows...use your preferred bash terminal. [Here is a site](https://www.computerhope.com/issues/ch001927.htm) that was updated relatively recently (June 2020) that includes instructions for getting started with git on windows. 

### 2. Check git:
`git --version`

### 3. Check your configuration variables
- If you already have git installed from a while ago, you can check your config variables to see if you already have some:
`git config --list`

### 4. Set up configuration variables
`git config --global user.name "YOUR NAME HERE"`
`git config —globe user.email "YOUR EMAIL HERE"`

### 5. Navigate to the folder you would like to be working in
`cd berkeley/tutorials`

### 6. Initiate an empty local git repository
`git init`

### 7. Connect your local folder location to a remote repository on github
- Go to github.com, sign in
- navigate into the repository you've created for this project, and at the top right of the screen, click the green 'Code' button. 
- Copy the https URL, and return to the terminal:
`git remote add origin [paste URL here]`

### 8. Pull changes from github
`git pull origin main`

### 9. Create a .gitignore file
- This is where you can specify which files/folders that you DON'T want sent to github from your local workspace.
`touch .gitignore`
`vi .gitignore`
- press 'i' for insert and start writing
- add file names to ignore, or folders
	- folders should be written like this: `folder-i-dont-want-on-github/`
- press `<ESCAPE>` to get out of write mode onec you are finished
- `:wq` and then `<ENTER>` will quit and save changes.

### 10. Submit local changes to git
`git add .`

### 11. Check to see whether changes have been incorporated
`git status`

### 12. Write a commit message: describe the changes you made
`git commit -m "first commit"`

### 13. Push changes to your remote repository on github
`git push -u origin main`
- NOTE: you only have to use the `-u` flag for the FIRST push. Later, you can just write `git push origin main.`

## Troubleshooting and other useful commands for when mistakes are made...
### To remove a remote repository from your local working directory:
`git remote rm [name of remote]`

### To un-add changes to git from the local repository & start over
`git reset`

### to get rid of an empty git repo in your local working directory
`rm -rf .git`

### to get rid of newly created test files that you don't want
`rm test.txt test2.txt`