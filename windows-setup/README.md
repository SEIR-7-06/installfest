# Installfest for Windows: Welcome to the Party

## You've Got Choices

The majority of the tools we use in this course *exist* for Windows, but many of them work slightly differently, require specialized setup, and won't include most of the specific packages and frameworks we'll use in this course.

#### There are four options for how you might proceed, listed in order of best-likely-outcome to worst-likely-outcome.

### 1. Get a Mac

While this is probably not what you're hoping to do, getting a Mac is the best way to ensure that your computer doesn't get in the way of you becoming a successful developer in this course (and beyond). A Mac computer is also increasingly the [more popular and recommended setup for software engineering](https://www.macworld.co.uk/feature/apple/why-programmers-think-mac-os-x-is-best-os-use-3638706/). **For about half of students who start the course using a Windows computer, they purchase a Mac by the end of the course because of their frustrations with using Windows.** Your instructors, while helpful and knowledgable, are less able to help you debug problems with installing tools on a Windows computer, and **your instructors cannot be your technical/installation support if you choose any of the other three options. It will be your responsibility to solve these problems; your instructors can only provide very limited support.**

If getting a Mac is infeasible for you, or you want the challenge, or you're an expert user, the other available options are:

### 2. Install Linux

Because Linux and MacOS are both Unix-based systems, the tools we use in this course are also available and will work in the same ways as Macs for Linux. While your instructor still won't be able to troubleshoot installation issues, or tell you what steps to follow to install pieces of software, you will be able to run the tools used in this class.

If you're comfortable setting up your computer to dual-boot Linux, that has been most effective for GA students in the past. Or, if partitions make you cranky, some students have been successful using VirtualBox to install a Linux VM; this is likely to cause you more issues than dual-booting, but it requires less know-how.

### 3. Use Windows and Git Bash

Git Bash is a tool provided by GitHub to mimic the functionality of a Unix-based system on a Windows machine. This choice will require you to investigate for yourself how to install and run each of the tools we use in the course; you'll be installing the Windows version of those tools, then attempting to use them from a combination of the Windows shell and the Git Bash shell. I have seen one student attempt this setup before, and by the middle of the course, they bought a Mac, because they had run into so many issues with the slight differences between how frameworks and applications run on the different operating systems.

### 4. Use the Windows Subsystem for Linux

#### WARNING: These instructions will lead to an unstable setup.
The Windows Subsystem for Linux is an unstable system, and has many bugs that will make your life more difficult for using it. Having gone through the (long, complicated) setup process detailed in the following pages, because of significant bugs within the system, **it is easy to enter one command incorrectly and lose all of your installed programs**.

#### To repeat: DO NOT follow these instructions unless you have no other option, or the Windows Subsystem for Linux is out of beta.

With that out of the way, here are the directions that will allow you to use the WSL.

1. Set up your **Development Environment**:
    * [ ] [The BASH Command Line](dangerous-wsl-setup/bash-setup.md)
    * [ ] [Developer Tools](dangerous-wsl/setup/developer-tools.md)
2. Set up your **Web Technologies**:
    * [ ] [Node Stack](dangerous-wsl-setup/node-setup.md)
