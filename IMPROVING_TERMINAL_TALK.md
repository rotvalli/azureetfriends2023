# Improving terminal

Command line is a key tool for many of us. On *nix world the bash is still the default shell/langauge with really long history. PowerShell has challenged that and is a good modern option. 

But what if there would be something different with some new ideas?

## Introducing Nushell

Nu draws inspiration from projects like PowerShell, functional programming languages, and modern CLI tools. Rather than thinking of files and data as raw streams of text, Nu looks at each input as something with structure. For example, when you list the contents of a directory what you get back is a table of rows, where each row represents an item in that directory. These values can be piped through a series of steps, in a series of commands called a 'pipeline'.

## Installing Nushell

macOS / Linux:

    brew install nushell

Windows:

    winget install nushell