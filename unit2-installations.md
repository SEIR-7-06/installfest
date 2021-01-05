# Installfest Step 1.1: Node.js & Express Stack

Most of the coding work we do in weeks 3 to 5 will be driven by the back-end web development framework [Express](http://expressjs.com). We'll install Express individually in each project we create. For now, we'll install the other tools we'll use along with Express.

#### Plan Overview

1. Install Node.js, a platform for back-end web development with the JavaScript programming language.
1. Install MongoDB, the database we'll use with our Node.js and Express stack.

## Node.js

We're going to install Node.js using a tool called Node Version Manager (NVM for short). Node has been around for a while and has many versions available for us to use. We're going to focus on the latest Longterm Support (LTS) version for our work in the course.

1. Run the following command to download the `nvm` install script via `curl`:

```bash
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
```

2. Double check that NVM installed correctly with:

```bash
nvm --version
```

3. Finally we're ready to install Node. We want the latest LTS version. To get it and use it, run these commands:

```bash
nvm install --lts
```

> Your console should display a progress bar during installation. Wait for this to complete before continuing.

```bash
nvm use --lts
```

> Set the default Node version
```bash
nvm alias default node
```

### Nodemon

Nodemon (short for "node monitor") will make our Node.js workflow more efficient.

1. Install nodemon globally with the following Terminal command:

```bash
npm install -g nodemon
```

## MongoDB

MonogDB is a database that stores information as easy to read "documents". We'll use it to store data in our Node.js and Express stack.

1. To install Mongodb please follow the install instructions on their site for your operating system.

[Install Instructions](https://docs.mongodb.com/manual/administration/install-community/)


2. After the installation, run the `which` command to verify the install was successful.

```bash
which mongo
```

If this has worked correctly, you will see `/usr/local/bin/mongo` as the output from terminal.

## Robo3T

Robo3T is a GUI (Graphical User Interface) tool to let us see the data in our Mongo databases. Let's install that now.

1. Go to [https://robomongo.org/download](https://robomongo.org/download) and download the free (community) edition.
2. Install it!

## Next Up

- [Install Visual Studio Code](./mac-dev-tools/editor-vsc.md)

![](https://media.giphy.com/media/l3dj09hpsfuYkijDi/giphy.gif)
