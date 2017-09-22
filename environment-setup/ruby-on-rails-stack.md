# Installfest Step 1.2: Ruby on Rails Stack

#### Here's the plan... (just an overview)

1. Update your install of the Ruby programming language and install rvm to manage versions of Ruby.
2. Install Rails, a back-end web development framework for the Ruby programming language.
3. Install PostgreSQL, the database we'll use with our Ruby on Rails stack.

## Do you already have ruby, rails or rvm? If yes, make sure they're up to date.

If you've already experimented with Ruby and/or Rails before, verify that your versions are correct for this upcoming class.

1. In your Terminal, run `ruby --version`. The output will include the version number of Ruby you have installed. **Verify you are running version 2.2+ of Ruby and that it does not say `universal.x86-64`**.  The `universal` build is the one that comes with OS X, we want to use a ruby version supplied by RVM.
2. In your Terminal, run `rails --version`. **Verify you are running version 5 of Rails**.
3. In your Terminal, run `rvm list`.  **Verify you have version 1.26.x or greater.**

If you are using an earlier version of RVM, Ruby or Rails, continue with the instructions to get your environment set up. Run these version commands in the Terminal again after you're done to ensure everything is working properly.

## RVM and Ruby

__Note:  when copying the code snippets, please exclude the `$` as you paste and run the code into your terminal.  The dollar sign `$` is simply an indicator of the logged-in user's terminal prompt in examples.__

[RVM](https://rvm.io) is a Ruby Version Manager. It lets you easily switch between versions of the Ruby programming language for different projects.

1. Run the following command in your Terminal to install both RVM and the latest version of Ruby.

<!--
**Note for August 2017 cohort ONLY:** Due to a current bug in the RVM installer, you should NOT run the command below, and should instead run:
```
\curl -sSL https://raw.githubusercontent.com/wayneeseguin/rvm/stable/binscripts/rvm-installer | bash -s stable --ruby
```
-->

  ```bash
  $ curl -L https://get.rvm.io | bash -s stable --ruby --auto-dotfiles
  ```

  This installation could take a few minutes, so don't panic if it's slow.

2. Close your terminal and open a new one now.

3. Run
  ```bash
  $ gem install bundler
  ```

## Rails 5

Ruby packages are referred to as "gems".

1. Use the following Terminal command to install Rails 5.

  ```bash
  $ gem install rails
  ```

  This might take a few minutes.  
  If this causes errors on your machine, ask for help.

## PostgreSQL  

### Postgres

1. Install postgres via Homebrew
  ```bash
  $ brew install postgres
  ```

2. Configure postgres to start when the system does.

  ```bash
  $ brew services start postgresql
  ```


3. Check that your install worked

    ```bash
    $ which psql
    ```

    If it worked, you should see ```/usr/local/bin/psql``` as the terminal output.



## Next Up
* [x] Set up your Node.js environment
* [x] Set up your Ruby environment
* [ ] [Install Development Tools](/mac-dev-tools)
