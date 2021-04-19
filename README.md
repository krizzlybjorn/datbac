# datbac

## Virtualenv
##### Do once (Kristoffer)
> pip install virtualenv

Create virtual env:
> python -m venv venv

> pip install ipykernel

Add virtual environment to Jupyter Notebook:
> python -m ipykernel install --user --name=venv


Close VScode.
### Working with virtual env ###
Always choose virtual environment on the top right kernel.
When working on new notebook.

Activate virtual env (do this when working on project):
> venv\Scripts\activate (windows)
> 
> source venv/bin/activate (linux)


Deactivate (when finished working):
> deactivate


Add requirements in venv:
> pip install ..package..


Make requirements:
> pip3 freeze > requirements.txt

### For users ###
Install requirements:
> pip install -r requirements.txt


## Git commands ##
Clone this repository SSH:
> git clone git@github.com:krizzlybjorn/datbac.git

Push to this repository:
> git push

Create a branch and switch to it:
> git checkout -b branchname

Delete a branch:
> git branch -d branchname

Switch back to master branch and clean local repository:
> git checkout master
>
> git fetch origin
>
> git reset --hard origin/master
>
> git clean -ffdx

### How to edit a commit after it has been pushed ###
##### Take great care when using this, as rewriting the history could mess up everything for everyone

Start by finding the commit
> git log --oneline

Use rebase interactive on the commits from HEAD untill you reach the commit. If it is the latest commit, use 1.
> git rebase -i HEAD~1
>
> git rebase -i HEAD~n

Git will now open a texteditor. Change the "pick" keyword to "e" or "edit" for the commit. 
##### DO NOT REMOVE OR CHANGE THE OTHER LINES.
Save and close

Edit whatever was wrong with the commit.

Stage the changes
> git add foobar

Commit the changes using amend. Optionally, use also "no-edit" to leave the commit message unchanged.
> git commit --amend --no-edit

If everything looks good, complete the rebase and push.
> git rebase --continue
> 
> git push -f

Abort the rebase if needed.
> git rebase --abort