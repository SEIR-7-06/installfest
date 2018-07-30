## Visual Studio Code Text Editor

1. Go [here](https://code.visualstudio.com/) to download Code.
2. Open the downloaded zip file.
3. Drag the unzipped `Visual Studio Code` app to your `Applications` folder.

## Add Packages
Visual Studio Code's core functionality can be extended using thousands of third-party packages that can help reduce your errors, and increase your productivity.

We can install VSC packages in the VSC extensions sidebar. Since we're learning to be awesome developers now, let's add an extension!

1. In the search bar, search for `indent-rainbow`.
2. When you have found the package, click on the green `install` button.
3. You may be prompted to reload your Visual Studio Code. That's perfectly fine!  
4. After reloading, you will now have that extension installed and activated!
5. Try searching for and adding the `open in browser` extension as well for more practice. 

> Note: As a new developer, you might not need many extensions to start. Get a feel for VSC a while before adding to it.

## Add the command `code` to the terminal to open Visual Studio Code
1. With VSC open, type this shortcut to pull up the command pallette:  
` command + shift + P `
2. Enter the command `install 'code' command in PATH` and press enter.
3. Now you will be able to type `code` in the terminal to open VSC!`

## Configure Git to Use Visual Studio Code
When you forget to enter a commit message in the Terminal, git opens a text editor and reminds you to add a commit message.

Run the following command in the Terminal to configure git to open Code instead of the default text editor:

```bash
$ git config --global core.editor "code --wait"
```
