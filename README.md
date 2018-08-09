# Automatic Backup System (ABS)


## Overview

ABS uses CRON to periodically check your GIT repositories and push any changes to a designated remote.  
*ABS was not intended for collaboratively work, but instead a lazy backup method for loose scripts*  


## Usage

### ABS Remote Add

* Example #1: Add a remote by name.  
    * `abs-remote-add --remote-name bitbucket` outputs `cd 'common/dot/.git' && git remote add bitbucket git-common-dot`

* Example #2: Add a remote by name & directory.  
    * `abs-remote-add --remote-name bitbucket --directory /tmp` outputs `cd '/tmp/common/dot/.git' && git remote add bitbucket git-common-dot`

* Example #3: Add a remote by name & prefix.  
    * `/git/develop/script/abs/bin/abs-remote-add --dry-run --remote-name bitbucket --directory common --remote-prefix "git@bitbucket.org:tiye/"` outputs `cd 'common/dot/.git' && git remote add bitbucket git@bitbucket.org:tiye/common-dot`

* Example #4: Add a remote by name, prefix & suffix.  
    * `/git/develop/script/abs/bin/abs-remote-add --dry-run --remote-name bitbucket --directory common --remote-prefix "git@bitbucket.org:tiye/" --remote-suffix ".git"` outputs `cd 'common/dot/.git' && git remote add bitbucket git@bitbucket.org:tiye/common-dot.git`

* Example #5: Add a remote by name, prefix, suffix & strip 'common-'.  
    * `/git/develop/script/abs/bin/abs-remote-add --dry-run --remote-name bitbucket --directory common --remote-prefix "git@bitbucket.org:tiye/" --remote-suffix ".git" --remote-strip "common-"` outputs `cd 'common/dot/.git' && git remote add bitbucket git@bitbucket.org:tiye/dot.git`

### ABS Remote Remove

* Example #1: Remove a remote by name.  
    * `abs-remote-remove --remote-name bitbucket` outputs `cd 'common/dot/.git' && git remote remove bitbucket`

* Example #2: Remove a remote by name & directory.  
    * `abs-remote-remove --remote-name bitbucket --directory "/tmp"` outputs `cd '/tmp/common/dot/.git' && git remote remove bitbucket`

### Note(s)

* All command(s) support the `--dry-run` option. This allows you to inspect output before changes are applied.  
*It is highly recommended to run all commands with the `--dry-option` to inspect output before commiting changes.`  


