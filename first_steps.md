# First Steps #

Okay, that's all well and good but we don't have a website and that means no one is getting paid. We started out with networks of computers, now let's focus on your computer. The first thing you need to do is throw away your mouse. The keyboard is your friend and getting proficient at using it will save you insane amounts of time. Typing isn't really what it's all about, it's about getting familiar with commands. The command line interface (CLI) will you be frustrating at first but that's okay, everything is frustrating until you master it. First, open up your command line. On Windows, use PowerShell (search for it in the start menu, just don't pick the ISE that's not what we're doing here yet) for Mac, use Finder to get your Terminal running. If you use Linux, this is probably a little beneath you so feel free to skip ahead if you like.

## Some conventions
In this text we will have console input and output. Input will look like this:

```PowerShell
PS Q:\ > my-command --with -aflag and text 
```
Notice that it will look a little bit different in the terminal window since Markdown doesn't like having :\> without spaces. 
While output will look like this.
```PowerShell
PS Q:\ > my-command --with -aflag and text 
Thanks for using my-command!
```

Sometimes we will just want some inline commands like ```cd myproject``` so context will describe what to do with these.

## Hello World
The first thing we'll do in any language is the cannonical 'Hello World' program so let's get started.
Hopefully that terminal is fired up, here we go:

```PowerShell
PS Q:\ > echo 'Hello World'
```
You should see:

```PowerShell
PS Q:\ > echo 'Hello world'
Hello world
```

If you did see that: CONGRATULATIONS! 
If you didn't see that: Read the 'helpful' error message about why that went wrong.

One reason that could happen is you don't have an alias for 'Write-Output' called 'echo.' So what's an alias and what's this ```Write-Ouput``` business? Since Windows is quite ubiquitous as an operating system and many people will be forced to use it (especially those who prefer to use Linux) will want to be able to be productive in this environment so PowerShell (should) come with some aliases for Unix-Style commands. That is, if you know the command in Unix-Style, there is probably an equivalent command in PS with an alias. Our first command ```echo``` is the Unix-Style command for what PowerShell calls ```Write-Ouput```. The pattern of all PowerShell commands is: ```Verb-Noun``` where verbs include words like: get, set, start, stop, write, etc.. The Noun is going to be an object like a file (or file stream), a service (or Daemon in linux/unix), or really anything a computer knows how to deal with. 

## Exercise 1
This is going to be an easy one. I just want you to get a feel for what commands are available to you but not overwhelm.

Part 1
Fire up PowerShell and type:
```PowerShell
PS Q:\ > Get-Alias
```
What you should see:
A big table of commands and their aliases. 