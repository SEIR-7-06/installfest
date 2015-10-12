# Installfest Step 3: Ruby on Rails Stack

**Plan overview:**

1. Update your install of the ruby programming language and install rvm to manage versions of ruby.
2. Install Ruby on Rails, a back end web development framework for the ruby programming language.
3. Install PostgreSQL, a database.

## Check Previous Installs

If you have already experimented with ruby or Ruby on Rails before, verify your versions are correct for this upcoming class.

1. In your Terminal, run `ruby --version`.  The output will include the version number of ruby you have installed. **Verify you are running 2.0+ of ruby**.

1. In your Terminal, run `rails --version`. **Verify you are running version 4 of Ruby on Rails**.


If you are using an earlier version of ruby or Ruby on Rails, continue with the instructions to get your environment set up. Run these version commands in the Terminal again after you're done to ensure everything is working properly.


##RVM and Ruby

<a href="http://www.rvm.io" target="_blank">RVM</a> is a Ruby Version Manager. It lets you easily switch between versions of the ruby programming language.

1. Run the following command to install both RVM and the latest version of Ruby.

    ```
    \curl -L https://get.rvm.io | bash -s stable --ruby
    ```

## Ruby on Rails 4

Ruby packages are referred to as "gems".  

1. Use the following command to install Ruby on Rails 4.
    
    ```
    gem install rails
    ```

1. If this causes errors on your machine, try running `sudo gem install rails` instead.


## PostgreSQL  

### Postgres.app (preferred)

1. Download <a href="http://postgresapp.com/" target="_blank">Postgres.app</a>.

2. Follow Postgress.app's install instructions (move Postgres.app into your Applications folder).
    
3. Follow Postgres.app's <a href="http://postgresapp.com/documentation/cli-tools.html" target="_blank">instructions to install command line tools</a>: 
  * add Postgres.app to your `$PATH`

      ```bash
        echo 'PATH=$PATH:/Applications/Postgres.app/Contents/Versions/9.4/bin' >> ~/.bash_profile
      ```
  * source your `~/.bash_profile`

      ```bash
      source ~/.bash_profile
      ```
  * check that your install worked
    
      ```bash
      which psql
      ```



#### Alternate install with homebrew

If you have already tried the Postgres.app instructions and spoken to a member of the teaching team, you may need to follow these <a href="http://exponential.io/blog/2015/02/21/install-postgresql-on-mac-os-x-via-brew/" target="_blank">instructions for installing postgreSQL with homebrew.</a>


