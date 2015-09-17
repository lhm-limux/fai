How to Keep the git Repository Up-to-date
=========================================

This text describes how to setup the local git repository to work within the
LHM development network.

Initial Setup
-------------

* We add the upstream git repository as remote "upstream"

        git remote add upstream git://github.com/faiproject/fai.git

* and download all content

        git fetch upstream 

* Then we make our local branches follow the upstream branches

        for remote in `git branch -r | grep -v /HEAD`; do branch=${remote:9}; git checkout -b upstream-$branch --track upstream/$branch; done


Github Mirror
-------------

All changes are stored on a github repository. These changes are then
automaticlly synced back into the LHM development network.

* Add the github mirror as remote "github"

	git remote add github git@github.com:lhm-limux/fai.git

Remember to push your changes to the remote "github"

 
