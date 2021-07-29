# Installfest Step 1.1: Node.js & Express Stack

Most of the coding work we do in weeks 3 to 5 will be driven by the back-end web development framework [Express](http://expressjs.com). We'll install Express individually in each project we create. For now, we'll install the other tools we'll use along with Express.

#### Plan Overview

1. Install Node.js, a platform for back-end web development with the JavaScript programming language.
<!-- 1. Install MongoDB, the database we'll use with our Node.js and Express stack. -->

## Node.js

We're going to install Node.js using a tool called Node Version Manager (NVM for short). Node has been around for a while and has many versions available for us to use. We're going to focus on the latest Longterm Support (LTS) version for our work in the course.

1. Verify you have a `.bash_profile`, `.zshrc`, and a `.zprofile` file in your home directory.
- Run `cd ~` to get into your home directory.
- Run `ls` and see if you have `.zprofile`, `.zshrc`, and `.bash_profile` in your home directory.
- If not, use the `touch` command to create those files. For example, `touch .zprofile` or `touch .bash_profile` or `touch .zshrc`
- Run `ls` again to verify that you have created those files.
- Quit out of your terminal completely. You can go to the top menu and select Terminal > Quit Terminal or press `cmd + q` on a Mac.
- Reopen your terminal application.

2. In the terminal, run `echo $0` to see what shell you are currently running in your terminal.
- If you get an output that says `-zsh` you are running the ZSH Shell.
- If you get an output that says`-bash` you are running the Bash Shell.

2. Install NVM

If you are running the ZSH Shell run this command to install NVM.
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | zsh
```

If you are not running ZSH and are using Bash, run this command instead to install NVM
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
```

After running the curl command quit out of your terminal completely again. You can go to the top menu and select Terminal > Quit Terminal or press `cmd + q` on a Mac.

3. Double check that NVM installed correctly with:

```bash
nvm --version
```

4. Finally we're ready to install Node. We want the latest LTS version (long term support version). To get it and use it, run these commands:

```bash
nvm install --lts
```

> Your console should display a progress bar during installation. Wait for this to complete before continuing.

5. Use the lts version of node.

```bash
nvm use --lts
```
This will give you the latest version of node you have installed.

6. Set the default Node version.
```bash
nvm alias default <your-latest-version>
```
for example
```bash
nvm alias default v14.17.4
```

### Nodemon

Nodemon (short for "node monitor") will make our Node.js workflow more efficient.

1. Install nodemon globally with the following Terminal command:

```bash
npm install -g nodemon
```

<!-- ## MongoDB

MonogDB is a database that stores information as easy to read "documents". We'll use it to store data in our Node.js and Express stack.

1. To install Mongodb please follow the install instructions on their site for your operating system.

[Install Instructions](https://docs.mongodb.com/manual/administration/install-community/)


2. After the installation, run the `which` command to verify the install was successful.

```bash
which mongo
```

If this has worked correctly, you will see `/usr/local/bin/mongo` as the output from terminal.

## MongoDB Compass

[MongoDB Compass](https://www.mongodb.com/try/download/compass) is a GUI (Graphical User Interface) tool to easily visualize our data in MongoDB. We'll install this one as well to help with development when we begin working with MongoDB.
 -->
<!-- 
## Robo3T

Robo3T is a GUI (Graphical User Interface) tool to let us see the data in our Mongo databases. Let's install that now.

1. Go to [https://robomongo.org/download](https://robomongo.org/download) and download the free (community) edition.
2. Install it!

## Next Up

- [Install Visual Studio Code](./mac-dev-tools/editor-vsc.md)

![](https://media.giphy.com/media/l3dj09hpsfuYkijDi/giphy.gif) -->
