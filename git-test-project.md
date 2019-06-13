### Git test project

1. Configure your computer to log your name and email while making changes
  - `git config --global user.name "<first> <last>"`
  - `git config --global user.email "<email address>"`

2. Download the Github repository to the current directory
  - `git clone https://github.com/<username>/<project_name>.git`
  - Saves the entire repository under `/current/working/directory/<project_name>/`
  - Alteratively, you can create the local repository first without having to download
    - `git init`
    - `git remote add origin https://github.com/<username>/<project_name>.git`
    - `origin` just means "remote repository"

3. Typical workflow
  - `echo "Hello world" >> file.txt` or create whatever new file you want in the repository directory
  - `git add file.txt` when creating a new file in the working directory, it must be "staged" with this command before it can be "commited"
  - `git commit -am "my first commit"` saves all changes to the local repository
    - `-a` stages all files that have been modified or deleted (without touching new files that haven't been added)
    - `-m "<commit description>"` add a short message about the commit
  - `git push origin master` "push" all commits save locally to the remote repository
  - `git pull origin master` "pull" all changes in the remote repository (combines the `fetch` and `merge` routines)
    - `git fetch` download everything from the remote repository, but doesn't change any of the local files
    - `git merge origin` then merges the changes into the local files

4. Branching
  - `git checkout -b my_branch` create a new branch that is a copy of the `master` branch
  - `echo "New line from my branch" >> file.txt` or modify the files however you would like
  - `git checkout master` move back into the master branch (notice that `file.txt` no longer has the new line in it)
  - `git merge my_branch` merges the changes made in my_branch into the current branch (i.e. the master branch)

5. Pull Request
  - When you are working on a project with many other people, you do not want to modify the master branch without having others review your code
  - Therefore, open up a "pull request" on GitHub, which allows you to write messages about the update and lets other contributers review your code before it gets merged into the master branch
