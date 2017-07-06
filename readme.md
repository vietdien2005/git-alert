git-alert
========

This bash script watch new commit of your repository 

Notice: Only on Linux, sorry Unix & Windows guys

Installation:
------------
Run command: 

	git clone https://github.com/vietdien2005/git-alert.git
	cd git-alert && chmod +x git-alert && sudo mv git-alert /usr/bin

And create your cron:

	crontab -l | { cat; echo "* * * * * git-alert /home/repo origin/master >/dev/null 2>&1"; } | crontab -

Or run command ` crontab -e ` and input this line:

	* * * * * git-alert /home/repo origin/master >/dev/null 2>&1

Usage:
----------

    git-alert <git_folder> <remote>/<branch>

Example:
----------

    git-alert /home/your_repo origin/master

