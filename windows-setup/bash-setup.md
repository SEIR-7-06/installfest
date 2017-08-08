# Installfest for Windows, Step 1: Bash on Windows

1. Follow [Microsoft's instructions](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide) to get Linux installed on your system.

2. Type `pwd` at the command line. If it gives a path similar to `/mnt/c/Users/yourname`, then you're in great shape! If it says that is not a recognized command, try running `bash` first and then `pwd`. If you get errors, please call over an instructor.

3. Run `apt-get update` to ensure your Linux installation is up to date.

4. Run
```bash
sudo apt-get -f install
```
to ensure all default packages are installed.

Excellent-you now have Linux installed on your computer, which will let you use the same commands as everyone else for the remainder of the course.

Next up: your developer tools!
1. Set up your **Development Environment**:
    * [x] The BASH Command Line
    * [ ] [Developer Tools](developer-tools.md)
2. Set up your **Web Technologies**:
    * [ ] [Node Stack](node-setup.md)
    * [ ] [Ruby on Rails Stack](ror-setup.md)
