# Laravel
This is for practice laravel from scratch.

## Set up
1. Installation of Valet
Valet requires macOS and Homebrew. Before installation, you should make sure that no other programs such as Apache or Nginx are binding to your local machine's port 80.
	* Install [homebrew](https://brew.sh/)
	* Install [composer](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-osx)
	Make sure the `~/.composer/vendor/bin` directory is in your system's "PATH".
	-> add `export PATH="$PATH:$HOME/.composer/vendor/bin"` to `.bash_profile` and then use command `source .bash_profile` to restart bash.
	* Run `valet` to check if valet is installed correctly.
	* Run `valet install`
2. Serving Sites
Once Valet is installed you're ready to start serving sites. Valet provides two commands to help you serve you Laravel sites: `park` and `link`.
** this time just use `park`.
	* Create a new direstory on your Mac by running something like `mkdir ~/Sites`.
	* Move to the directory you created `cd Sites` and run `valet park` This command will register your current working directory as a path that Valet should search for sites.
	* Create Laravel site within the direstory: `laravel new app`.
	* Open `http://app.dev` in your browser.