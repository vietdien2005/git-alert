git-alert
========

This bash script watch new commit of your repository 

Notice: Only on Linux, sorry Unix & Windows guys

Installation:
------------
Run command: 

	git clone https://github.com/vietdien2005/git-alert.git && cd git-alert 
	chmod +x git-alert && sudo mv git-alert /usr/bin

And create your crontab:

	crontab -l | { cat; echo "5 * * * * git-alert /home/your_repo origin/master >/dev/null 2>&1"; } | crontab -

Usage:
----------

    git-alert <git_folder> <remote>/<branch>

Example:
----------

    git-alert /home/your_repo origin/master

Create a crontab like:
	
	crontab -l | { cat; echo "1 * * * * git-alert /home/your_repo origin/master >/dev/null 2>&1"; } | crontab -



