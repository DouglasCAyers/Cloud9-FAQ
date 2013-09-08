Cloud9-FAQ
==========

Troubleshooting and FAQ of gotchas I've run into integrating with Cloud 9 and GitHub so I don't forget them.


Auth errors trying to push to github
====================================

    > git push
    > fatal: Authentication failed


Solution 1
----------

Ensure you've linked your cloud 9 and github accounts and added your cloud 9 ssh key to github.

1. Get your cloud 9 ssh key from your account page, https://c9.io/douglascayers

2. Add the key to your github account, https://github.com/settings/ssh


Solution 2
----------

If you cloned a project from github into your cloud 9 workspace, you need to change
the remote origin url to use SSH instead of HTTPS otherwise you'll get authentication errors.

    > git remote set-url origin git@github.com:DouglasCAyers/try_angularjs.git

