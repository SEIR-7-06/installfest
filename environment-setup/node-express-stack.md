# Installfest Step 1.1: Node.js & Express Stack

Most of the coding work we do in weeks 3 to 5 will be driven by the back-end web development framework [Express](http://expressjs.com). We'll install Express individually in each project we create. For now, we'll install the other tools we'll use along with Express.

#### Plan Overview

1. Install Node.js, a platform for back-end web development with the JavaScript programming language.
1. Install MongoDB, the database we'll use with our Node.js and Express stack.

## Node.js

__Note:  when copying the code snippets, please exclude the `$` as you paste and run the code into your terminal.  The dollar sign `$` is simply an indicator of the logged-in user's terminal prompt in the examples.__

We're going to install Node.js using a tool called Node Version Manager (NVM for short). Node has been around for a while and has many versions available for us to use. We're going to focus on the latest Longterm Support (LTS) version for our work in the course. 

1. Run the following command to download the `nvm` install script via `curl`:

  ```bash
  $ curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
  ```

2. Double check that NVM installed correctly with:

  ```bash
  $ nvm --version
  # Output should look something like:
  0.32.1
  
  ```

3. Finally we're ready to install Node. We want the latest LTS version. To get it and use it, run these commands:

  ```bash
  $ nvm install --lts
  # Your console should display a progress bar during installation. Wait for this to complete before continuing.
  
  $ nvm use --lts
  
  ```


### Nodemon

Nodemon (short for "node monitor") will make our Node.js workflow more efficient.

1. Install nodemon globally with the following Terminal command:

  ```bash
  $  npm install -g nodemon
  ```


## MongoDB

MonogDB is a database that stores information as easy to read "documents". We'll use it to store data in our Node.js and Express stack.

1. Use Homebrew to update all our brew packages.

  ```bash
  $ brew update
  ```

2. Run `brew install` for **MongoDB**.

  ```bash
  $ brew install mongodb
  ```

3. Then we'll need a directory for **MongoDB** to save data. Make sure you create this directory inside your root (`/`) directory.

  ```bash
  $ cd /
  $ sudo mkdir -p data/db
  ```

  You will be prompted to enter your system password here. This is the password you use to log into your computer.

  *Sidenote:
  When you use this  `sudo` command, you are saying "superuser do" which can force your computer to perform the command you entered, even if it's a bad idea. This is why you're prompted to insert a password. Terminal makes sure your computer is secure and that you're sure about the command you're about to execute forcefully.*

  ![relevant xkcd](https://cloud.githubusercontent.com/assets/6520345/17527880/f458616c-5e21-11e6-9156-4db012c5efc7.png)
  [Source: xkcd](https://xkcd.com/149/)

4. Finally we'll want to make sure we have permission to read and write to this directory.

  ```bash
  $ sudo chown -R $USER data/db
  ```
  Again, you'll need to enter your system password.

5. Run two commands to check whether the install worked. You should see a file path after each command.

  ```bash
  $ which mongod
  $ which mongo
  ```

  If this has worked correctly, you will see `/usr/local/bin/mongod` and `/usr/local/bin/mongo` respectively as the outputs from terminal.

## Robo3T

Robo3T is a GUI (Graphical User Interface) tool to let us see the data in our Mongo databases.  Let's install that now.

1. Go to [https://robomongo.org/download](https://robomongo.org/download) and download the free (community) edition.
2. Install it!

## Next Up
* [x] Set up your Node.js environment
* [ ] [Install Development Tools](https://git.generalassemb.ly/sf-wdi-45/installfest/tree/master/mac-dev-tools)
