#Installfest Step 2: Express Stack

Most of the coding work we do in weeks 3 to 5 will be driven by the back end web development framework <a href="http://expressjs.com/" target="_blank">Express</a>. We'll install Express as we go, on a project-by-project basis. For now, we'll install other tools we'll use along with Express.

**Plan overview:**

1. Install Node.js, a platform for back end web development with the JavaScript programming language. 
2. Install JSHint and its Sublime Text packages to get realtime JavaScript syntax hints.
3. Install MongoDB, a database. 

## Node.js

1. Install Node.js with homebrew by running the following command in the Terminal.

  ```
  brew install node
  ```


1. Run the Terminal command `which node` to check that Node.js was installed. You should see a file path. The Terminal command `node` changes your Terminal into a Javascript REPL ("Read Evaluate Print Loop"), like the right hand side of repl.it.  Type `control+C` twice to quite out of the REPL and return to the normal Terminal commands.  

1. Run the Terminal command `which npm` to check that npm is installed. The Node Package Manager, used through various `npm` commands, is a lot like Homebrew, except we'll use it for Node.js-specific tools instead of for general Mac tools. NPM packages are often called "node modules."

### Nodemon

Nodemon (short for "node monitor") will make our node.js workflow more efficient. 

Install nodemon globally with the following command:
  
  ```
  sudo npm install -g nodemon
  ```

### JSHint

It's time to install another Sublime Text package!

1. Select `Package Control: Install Package` to bring up the list of available packages.  Select `SublimeLinter` from the list, and Package Control will install it for you.

1. Repeat the step above to install the packages "SublimeLinter-jshint".

1. Sublime Text 3 has the packages we need, but we also have to install our linter program, jshint.  Back in the Terminal, run `sudo npm install -g jshint` to install jshint globally. 


## MongoDB

MonogDB is a popular database that stores information as easy to read "documents".  We'll use it to store data with our Express stack. 

1. Use homebrew to update all our brew packages.

  ```bash
  brew update
  ```
1. Run `brew install` for **MongoDB**

  ```bash
  brew install mongodb
  ```

1. Then we'll need a directory for **MongoDB** to save data.

  ```bash
  sudo mkdir -p /data/db
  ```

1. Finally we'll want to make sure we have permission to read and write to this directory.

  ```bash
  sudo chown -R $USER /data/db
  ```

1. Run two commands to check whether the install worked. You should see a file path after each command.

  ```bash
  which mongod
  which mongo
  ```
