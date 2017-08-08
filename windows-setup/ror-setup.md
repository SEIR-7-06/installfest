# Installfest for Windows, Step 4: Ruby on Rails

You're so close! The last step is to make sure you're prepared for the web technologies we use in the second half of the course.

## Installing Ruby

[RVM](https://rvm.io) is a Ruby Version Manager. It lets you easily switch between versions of the Ruby programming language for different projects.

1. Run the following command to install both RVM and the latest version of Ruby.

 **Note for August 2017 cohort ONLY:** Due to a current bug in the RVM installer, you should NOT run the command below, and should instead run:
 ```
 \curl -sSL https://raw.githubusercontent.com/wayneeseguin/rvm/stable/binscripts/rvm-installer | bash -s stable --ruby
 ```

  ```bash
  $ curl -L https://get.rvm.io | bash -s stable --ruby --auto-dotfiles
  ```

  This installation could take a few minutes, so don't panic if it's slow.

2. Run
```
echo "source $HOME/.rvm/scripts/rvm" >> ~/.bashrc
```

3. Close your command prompt and open a new one now.

4. Run
  ```bash
  $ gem install bundler
  ```

## Installing Rails

1. Run
```
gem install rails
```

## Installing PostgreSQL

1. Run
```
$ sudo apt-get install postgresql
```

2. We need to start the database running to finish setting it up. Run
```
$ sudo systemctl enable postgresql
$ sudo service postgresql start
```

3. We need to create ourselves as a database user in order to connect to the database. Run
```bash
$ sudo su postgres # briefly become the special postgres user
$ createuser -s YOUR-USERNAME-HERE # as the postgres user, add yourself as a user
$ exit # go back to being yourself
$ createdb YOUR-USERNAME-HERE # make yourself a database
$ psql # connect to that database
```
Call an instructor over if any part of those directions gives an error. If you see a weird command prompt that ends in a #, you've done it correctly! Hit Ctrl-D to exit.

## That's it!
![](http://i.giphy.com/3otPoS81loriI9sO8o.gif)

Thanks for coming to InstallFest, and we're excited to see you next week! Feel free to stick around and finish up Fundamentals, or head out.
