`sudo pacman -Syu`

* S: means Sync. alone it is used to install packages. But here together, it means that Pacman should use the "repository sync mode".

	Pacman has different operation modes:
		- S -> repository / remote packages
		- R -> remove packages
		- Q -> query installed packages
		- U -> install a local file.

* y: refresh This means, refresh the package database. So Pacman downloads the latest list of available packages from the mirrors.
* u: upgrade: Upgrade all installed packages to their latest versions.

In few words: Synchronize package databases, refresh them, and upgrade the entire system.


#tech #linux #packagemanager
