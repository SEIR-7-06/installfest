# 🛑 Unit 2-4 Installfest
**Stop!** The following instructions pertain to units 2-4 - revisit this section in unit 2!

## Unit 2 - PostgresQL
When it comes to installing database technologies - WSL has a handful of extra configuration steps as the installations will not work by default.

*  [PostgresQL Webpage](https://www.postgresql.org/download/linux/ubuntu/)
```
# Create the file repository configuration:
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

# Import the repository signing key:
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

# Update the package lists:
sudo apt-get update

# Install the latest version of PostgreSQL.
# If you want a specific version, use 'postgresql-12' or similar instead of 'postgresql':
sudo apt-get -y install postgresql
```

### WSL-specific configuration instructions
By default on WSL - running the `psql` command will give you an error similar to:

`psql: error: FATAL: role "<your_user_name>" does not exist`

## The fix:
* Run the following commands one by one, but change `<your_user_name>` to your linux username!
```
# Auto start the postgres server
sudo -u postgres pg_ctlcluster 13 main start

# Start the postgres server the first time
sudo service postgresql start

# Create a postgres user that matches your username
sudo -u postgres createuser <your_user_name>

# Create a postgres database that matches your username
sudo -u postgres createdb <your_user_name>

# Run psql as the postgres user
sudo -u postgres psql
```

* The last command will bring you inside of the `psql` shell - run the following command
```
ALTER USER <your_user_name> WITH SUPERUSER;
```


## Unit 3 - MongoDB

When it comes to installing database technologies - WSL has a handful of extra configuration steps as the installations will not work by default.

Follow allong w/ the Microsoft documentation and instructions for installing MongoDB:

https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-database#install-mongodb

1. Run `sudo service mongodb start` - if you see 'OK', then we're all set!

2. Run `mongo` to open the mongo shell!

However, if `sudo service mongodb start` results in 'FAIL' - you may need to manually start the `mongod` process yourself

   - Run `mongod`, then open a new tab. We'll leave the `mongod` tab alone to run the mongodb process in the background while we are working in a different tab.


## Unit 4 - Python
Python install instructions - run the following commands in your terminal
```
# install python
sudo apt-get install python3
sudo apt-get install python3-pip
```

In your `~/.zshrc` file, add the following lines
```
# Alias python to python3
alias python=python3
alias pip=pip3

# To allow pip packages to be in PATH
path+=(/home/<your_user_name>/.local/bin)
```

<hr />

## Navigation
1. Read this intro
    * [✔️] [Alternative OS intro](./README.md)  
2. Prior to the first day of class: Enable WSL and Install Ubuntu from the Microsoft Store app
    * [✔️] [WSL Setup](./wsl-setup.md)
3. On the first day of class, your instructors will help you with **Installfest**
    * [✔️] [Installfest](./wsl-installfest.md)
4. Optional visual and usability upgrades for your terminal
    * [✔️] [Upgrades](./upgrades.md)
5. Unit 2-4 Installfest
    * [✔️] [Unit 2, 3, 4 Installfest](./wsl-unit234.md)
