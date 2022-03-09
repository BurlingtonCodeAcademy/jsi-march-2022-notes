# House Keeping

From here on out, primary form of communication will be through discord. Please use our discord channel to share all your questions!

Class recordings are typically shared a few days after each class session.

# Keep In Mind

Users are our greatest teachers! They will break your program and you'll learn how to build it better!

There is no right way to find the answer/solve the problem...everyone can/will approach it differently-- This differentiation is part of what makes coding so exciting!

*Pattern recognition* is foundational to *Programmatic Thinking*. It can take time to build up this muscle and that's more than ok!

Errors can be frustrating, but have no fear! An error message allows us to better understand what needs to be fixed and how to fix it.

# Fun Facts

The very first reported *bug* was actually in 1947: a moth was trapped in the computer, oh my! Check it out: https://www.nationalgeographic.org/thisday/sep9/worlds-first-computer-bug/#:~:text=First%20Computer%20Bug-,Sep%209%2C%201947%20CE%3A%20World's%20First%20Computer%20Bug,their%20computer%20at%20Harvard%20University.

# CLI vs GUI

CLI is the Command Line Interface. The Command Line allows you to talk directly with your computer to access files/directories. 

GUI (pronounced: "Goo-ey") is the Graphic User Interface. It is less powerful than the CLI


# Moving Around

When moving around on the terminal you use the `cd` command with the *relative path* to your desired destination.

`cd /code` would move you from my current directory into a subdirectory named `code`

`cd ..` Will move you from your current directory to the containing directory. `..` means "go up one level from my current location."

You can use more complicated relative paths to go through multiple directories

`cntrl l` Will move your cursor to the top of your terminal window

`cd ../../labs/bug-hunts` would take you up two levels (into the location that contains the directory that contains the directory you started in) then it will look for a sub directory named `labs` and a further subdirectory named `bug-hunts` which is where you end up when you hit <kbd>Enter</kbd>.

You can also hit <kbd>Tab</kbd> to autofill directory names after typing the first couple characters.

## Location, Location, Location

In the terminal you are always *inside* a directory. When traveling through multiple directories it can be easy to get lost. There are a few helpful commands to show where you are.

If you're on MacOS you can use the command `pwd` to see where you are

If you're on a Windows machine your prompt in the command line will include the *full file path to your current location*. If you're using cmder you can also use the `pwd` command to print the full file path to your current location in the terminal.

The command `ls` will provide a list of all of the contents contained within the current directory you are in.

On Mac: To open finder via the CLI, use the command `open .`
On Windows: To open explorer via the CLI, use the command `start .`

`.` means *this location that I am in right now*

## Creating Things

You can create files in the terminal by using the `touch` command and specifying the file name.

`touch index.js` would create a new file named `index.js` inside the current directory

You can also make subdirectories with the `mkdir` command

`mkdir labs` would create a new subdirectory named `labs` inside the current directory

## Running Programs

Many programs have a CLI (command line interface) that allows them to be run through the terminal. These commands are specific to the applications, and you can usually find instructions on how to use them in the program's documentation.

There are two programs we will commonly access through the CLI throughout this course, NodeJS, and VSCode

The command for NodeJS is `node`. Entering `node` by itself will change your terminal into a Node environment

Entering the command `node index.js` from the terminal (**NOT A NODE ENVIRONMENT**) will run the file `index.js` if it exists in the current location.

The terminal command for VSCode is `code`. To open VSCode from the directory you're currently in you can use the command `code .`
