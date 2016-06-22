## Atom Text Editor

1. Go <a href="https://atom.io/" target="_blank">here</a> and download Atom.
2. Open the downloaded file.
3. Follow the installation instructions.
4. Open the Atom application.

### Add Packages

Let's install our first package, Emmet.  We can install Atom packages in the Atom settings menu, or via the command-line.  Since we're learning to be awesome developers now, let's use the command-line!

1. In your terminal run: `apm install emmet-simplified`

The other package we'll add, `jshint`, requires Node.js, so we'll get to it in the next set of installation instructions.

### Configure Git to Use Atom

When you forget to enter a commit message in the Terminal, git opens a text editor and reminds you to add a commit message.

1. Run the following command in the Terminal to configure git to open Atom instead of the default text editor:

    ```bash
    $ git config --global core.editor "atom -w"
    ```
