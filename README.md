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