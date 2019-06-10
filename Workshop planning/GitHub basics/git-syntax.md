### Git Syntax Reference

1. `git config`
- `--user.name "<first> <last>"`
- `--user.email "<email address>"`

2. `git clone https://github.com/<username>/<project_name>.git`
- "Download" the Github repository to the current directory
- Saves the entire repository under `/current/working/directory/<project_name>/`

3. `git init`
- Create a new local repository in the current working directory
- Use this instead of `git clone` if you would like to start working locally

4. Git names
- `origin` the "remote" Github repository (i.e. `https://github.com/<username>/<project_name>.git`)
- `master` the primary "branch" of the repository

5. Workflow
- `git add <file>` when creating a new file in the working directory, it must be "staged" with this command before it it "commited"
- `git commit` saves all changes since your last commit
  - `-a` stage all files that have been modified or deleted (without touching new files that haven't been added)
  - `-m "<commit description>"` add a short message about the commit
- `git push origin master` "push" all commits save locally to the remote repository
- `git pull` "pull" all changes in the remote repository (combines the `fetch` and `merge` routines)
  - `git fetch` download everything from the remote repository, but don't change any of the local files
  - `git merge origin`

6. Branching
- `git checkout -b <branch_name>` create a new branch that is a copy of the `master` branch
- `git checkout <branch_name>` move between branches
- `git merge <branch_name>` merges the changes made in "source branch" into the current branch (i.e. `git checkout master` before running this)
- `git rebase master` update the commit history of your current branch with the master branch commits that occured since you created your branch
