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

3. Installation of Dependencies
	* Run `composer install`
	* Run `npm install`

4. Adding BrowserSync
[BrowserSync](https://browsersync.io/) can automatically monitor your files for changes, and inject your changes into the browser without requiring a manual refresh. You may enable support by calling the `mix.browserSync()` method.
	* Add `mix.browserSync('my-domain.dev')` to `webpack.mix.js`
	* Run `npm run watch`
-> if error says `yarn: command not found`, run `brew install yarn` then run `npm run watch` again.

5. Database Set up
	* Run `php artisan make:model -m -c name-of-model` to create model, controller, and migration
	* Create columns in databaes/migrations/your_table_name
	* Run `php artisan migrate` to generate table
-> to refresh, run `composer dumpautoload` then `php artisan migrate:refresh`
-> if you don't have mysql setted up, run `brew install mysql` and `brew services start mysql`
-> you can connect to the database, at `127.0.0.1` using `root` username and an empty string for password.
-> if database is not created, `php artisan migrate` returns an error so create database first!!