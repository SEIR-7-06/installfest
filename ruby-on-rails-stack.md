# Installfest Step 3: Ruby on Rails Stack

## Check Previous Installs

If you've already experimented with Ruby and/or Rails before, verify that your versions are correct for this upcoming class.

1. In your Terminal, run `ruby --version`. The output will include the version number of Ruby you have installed. **Verify you are running version 2.0+ of Ruby**.
2. In your Terminal, run `rails --version`. **Verify you are running version 4 of Rails**.

If you are using an earlier version of Ruby or Rails, continue with the instructions to get your environment set up. Run these version commands in the Terminal again after you're done to ensure everything is working properly.

## RVM and Ruby

**Note:** When copying the code snippets, exclude the `➜` as you run the code in your Terminal. The `➜` is simply an indicator of the user in the Terminal.

<a href="http://www.rvm.io" target="_blank">RVM</a> is a Ruby Version Manager. It lets you easily switch between versions of the Ruby programming language for different projects.

1. Run the following command in your Terminal to install both RVM and the latest version of Ruby.

  ```zsh
  ➜  \curl -L https://get.rvm.io | bash -s stable --ruby
  ```

## Rails 4

Ruby packages are referred to as "gems".

1. Use the following Terminal command to install Rails 4.

  ```zsh
  ➜  gem install rails
  ```

  If this causes errors on your machine, try running `sudo gem install rails` instead.

## PostgreSQL  

### Postgres.app (preferred)

1. Download <a href="http://postgresapp.com" target="_blank">Postgres.app</a>.

2. Follow Postgress.app's install instructions (move Postgres.app into your Applications folder).

3. Follow Postgres.app's <a href="http://postgresapp.com/documentation/cli-tools.html" target="_blank">instructions to install command line tools</a>:
  
  * Add Postgres.app to your `$PATH`

    ```zsh
    ➜  echo 'PATH=$PATH:/Applications/Postgres.app/Contents/Versions/9.4/bin' >> ~/.zshrc
    ```

  * Source your `~/.zshrc`

    ```zsh
    ➜  source ~/.zshrc
    ```

  * Check that your install worked

    ```zsh
    ➜  which psql
    ```

### Alternate Install with Homebrew

**Only if the Postgres.app instructions above were unsuccessfully and you have spoken to a member of the teaching team**, follow these <a href="http://exponential.io/blog/2015/02/21/install-postgresql-on-mac-os-x-via-brew" target="_blank">instructions for installing PostgreSQL with Homebrew.</a>