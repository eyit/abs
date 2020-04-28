# Automatic Backup System (ABS) #

Recursively manage git repositories for backup.

## Getting Started ##
These instructions will get you a copy of the project up and running on your local machine.

### Installation ###

Clone the repository from github.  
``git clone https://github.com/eyit/abs.git``  
  
  
## Notes ##
  
Not intended for collaborative work; untested.  
  
Use the argument ``--dry-run`` to output commands before use.  
  
Vendor passwords are stored in plain text in ``$HOME/.config/abs``.  
  
  
## Usage ##

### Commands ###
  
#### abs fetch ####
  
Perform a recursive search on current directory and perform ``git fetch`` for each repo.  
``abs fetch``  
  
See additional options such as `--directory DIRECTORY` by adding the argument ``--help``.  
``abs fetch --help``  
  
  
#### abs pull ####
  
Perform a recursive search on current directory and perform ``git pull`` for each repo.  
``abs pull``  
  
See additional options such as `--directory DIRECTORY` by adding the argument ``--help``.  
``abs pull --help``  
  
  
#### abs push ####
  
Perform a recursive search on current directory and perform ``git push`` for each repo.  
``abs push``  

See additional options such as `--directory DIRECTORY` by adding the argument ``--help``.  
``abs push --help``
  
  
#### abs remote add ####
  
Add a remote with the name ``bitbucket``:  
``abs remote add --remote-name bitbucket``  
  
Add a remote by name and specify the directory to search.  
``abs remote add --remote-name bitbucket --directory /git``.  
  
See additional options such as `--prefix PREFIX` and ``--suffix SUFFIX`` by adding the argument ``--help``.  
``abs remote add --help``  
  
  
#### abs remote remove ####
  
Remove a remote with the name ``bitbucket``.  
``abs remote remove --remote-name bitbucket``  
  
See additional options such as `--directory DIRECTORY` by adding the argument ``--help``.  
``abs remote add --help``  
  
  
#### abs remote vendor bitbucket ####
  
Initialise ``bitbucket`` vendor by adding the ``init``, ``--username`` and ``--password`` arguments.  
``abs remote vendor bitbucket init --username USERNAME --password PASSWORD``  
  
Create a remote repository.  
``abs remote vendor bitbucket create --repository REPOSITORY``  
  
List remote repositories.  
``abs remote vendor bitbucket list``  

Remove a remote repository.  
``abs remote vendor bitbucket remove --repository REPOSITORY``  
  
  
