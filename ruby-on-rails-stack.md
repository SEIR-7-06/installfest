# Installfest Step 3: Ruby on Rails Stack

#### Plan Overview

1. Update your install of the Ruby programming language and install rvm to manage versions of Ruby.
2. Install Rails, a back-end web development framework for the Ruby programming language.
3. Install PostgreSQL, the database we'll use with our Ruby on Rails stack.

## Check Previous Installs

If you've already experimented with Ruby and/or Rails before, verify that your versions are correct for this upcoming class.

1. In your Terminal, run `ruby --version`. The output will include the version number of Ruby you have installed. **Verify you are running version 2.0+ of Ruby and that it does not say `universal.x86-64`**.
2. In your Terminal, run `rails --version`. **Verify you are running version 4 of Rails**.
3. In your Terminal, run `rvm list`.  **Verify you have version 1.26.x or greater.**

If you are using an earlier version of RVM, Ruby or Rails, continue with the instructions to get your environment set up. Run these version commands in the Terminal again after you're done to ensure everything is working properly.

## RVM and Ruby

__Note:  when copying the code snippets, please exclude the `$` as you paste and run the code into your terminal.  The dollar sign `$` is simply an indicator of the logged-in user's terminal prompt in examples.__

<a href="http://www.rvm.io" target="_blank">RVM</a> is a Ruby Version Manager. It lets you easily switch between versions of the Ruby programming language for different projects.

1. Run the following command in your Terminal to install both RVM and the latest version of Ruby.

  ```bash
  $ \curl -L https://get.rvm.io | bash -s stable --ruby
  ```

2. Close your terminal and open a new one now.

3. Run
  ```bash
  $ gem install bundler
  ```

## Rails 4

Ruby packages are referred to as "gems".

1. Use the following Terminal command to install Rails 4.

  ```bash
  $ gem install rails
  ```

  This might take a few minutes.  At the end you should see something like:
  ```bash

  ```
  If this causes errors on your machine, ask for help.

## PostgreSQL  

### Postgres.app (preferred)

1. Download <a href="http://postgresapp.com" target="_blank">Postgres.app</a>.

2. Follow Postgress.app's install instructions (move Postgres.app into your Applications folder).

3. Follow Postgres.app's <a href="http://postgresapp.com/documentation/cli-tools.html" target="_blank">instructions to install command line tools</a>:
  * Add Postgres.app to your `$PATH`

    ```bash
    $ echo 'PATH=$PATH:/Applications/Postgres.app/Contents/Versions/9.4/bin' >> ~/.bash_profile
    ```

  * Source your `~/.bash_profile`

    ```bash
    $ source ~/.bash_profile
    ```

  * Check that your install worked

    ```bash
    $ which psql
    ```

### Alternate Install with Homebrew

**Only if the Postgres.app instructions above were unsuccessfully and you have spoken to a member of the teaching team**, follow these <a href="http://exponential.io/blog/2015/02/21/install-postgresql-on-mac-os-x-via-brew" target="_blank">instructions for installing PostgreSQL with Homebrew.</a>
