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

## Quick tour

 - https://www.nushell.sh/book/quick_tour.html


## Working with files

0. Open a file without Nushell

   open sample.json

1. Same with Nushell

   open sample.json      

1. Open a file

    open kulutus.xlsx

2. Extract certain data from the file

    get Sheet1

3. Save the extracted data to a new format

    save kulutus.csv

4. Piped together

    open kulutus.xlsx | get Sheet1 | save kulutus.csv | tail kulutus.csv

## Fun with Azure

    az consumption usage list --only-show-errors

## Custom report

    az consumption usage list --only-show-errors | from json | select product pretaxCost | uniq-by product | sort-by -r pretaxCost | rename Palvelu Hinta | to csv


## Homework
Experiment with eye candy

    'Azure & Friends' | ansi gradient --fgstart '0x40c9ff' --fgend '0xe81cff' 
