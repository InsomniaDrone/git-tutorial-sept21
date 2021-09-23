
# Open the terminal
# On a mac, type 'terminal' in spotlight (or iTerm2 if you prefer)
# On windows...TBD

Check git:
`git --version`

# Check your configuration variables
## If you already have git installed from a while ago, you can check your config variables to see if you already have some:
`git config --list`

# Set up configuration variables
`git config --global user.name "YOUR NAME HERE"`
`git config —globe user.email "YOUR EMAIL HERE"`

#Navigate to the folder you would like to be working in
`cd berkeley/tutorials`

# Initiate an empty local git repository
`git init`

# Connect your local folder location to a remote repository on github
## Go to github.com, sign in
## navigate into the repository you've created for this project, and at the top right of the screen, click the green 'Code' button. 
## Copy the https URL, and return to the terminal:
`git remote add origin [paste URL here]`

#Pull changes from git
`git pull origin main`

# Create a .gitignore file
`touch .gitignore`
`vi .gitignore`
- press 'i' for insert and start writing
- add file names to ignore, or folders
	- folders should be written like this: `folder-i-dont-want-on-github/`
- press `<ESCAPE>` to get out of write mode onec you are finished
- `:wq` and then `<ENTER>` will quit and save changes.

# Submit local changes to git
`git add .`

# Check to see whether changes have been incorporated
`git status`

# Write a commit message: describe the changes you made
`git commit -m "first commit"`

# Push changes to your remote repository on github
`git push -u origin main`
- NOTE: you only have to use the `-u` flag for the FIRST push. Later, you can just write `git push origin main.`

# Troubleshooting and other useful commands for when mistakes are made...
## To remove a remote repository from your local working directory:
`git remote rm [name of remote]`

## To un-add changes to git from the local repository & start over
`git reset`

## to get rid of an empty git repo in your local working directory
`rm -rf .git`

## to get rid of newly created test files that you don't want
`rm test.txt test2.txt`