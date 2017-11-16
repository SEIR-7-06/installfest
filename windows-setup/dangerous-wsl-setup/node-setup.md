# Installfest for Windows, Step 3: Node

These directions (and all following directions) REQUIRE that you successfully installed Linux in [the first step](bash-setup.md).

## Node.js
Inside of a bash shell (i.e., after running `bash`):

1. Run
```bash
$ sudo apt-get install -y nodejs
$ sudo apt-get install -y nodejs-legacy
$ sudo apt-get install -y npm
```
Read the output and ensure that everything has installed correctly.

2. Using your newly-installed npm, install nodemon to help run our node apps more efficiently.
```bash
$ sudo npm install -g nodemon
```

## MongoDB

1. Follow the [MongoDB instructions for Ubuntu](https://docs.mongodb.com/v3.4/tutorial/install-mongodb-on-ubuntu/) through the end. After finishing the installation, run `which mongod` (yes, `mongod` with a d) to check that it's installed.

2. Run
```bash
$ cd /
$ sudo mkdir -p data/db
$ sudo chown -R YOUR-USERNAME-HERE data/db
```
to set up the directory where MongoDB will store its data.

## RoboMongo

RoboMongo is a GUI (Graphical User Interface) tool to let us see the data in our Mongo databases.  Let's install that now.

1. Go to [https://robomongo.org/download](https://robomongo.org/download) and download the free (community) edition.
2. Install it!


Awesome work! Last up: the Ruby on Rails Stack!
1. Set up your **Development Environment**:
    * [x] The BASH Command Line
    * [x] Developer Tools
2. Set up your **Web Technologies**:
    * [x] Node Stack
    * [ ] [Ruby on Rails Stack](ror-setup.md)
