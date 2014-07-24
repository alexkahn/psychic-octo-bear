# First Steps #

Okay, that's all well and good but we don't have a website and that means no one is getting paid. We started out with networks of computers, now let's focus on your computer. The first thing you need to do is throw away your mouse. The keyboard is your friend and getting proficient at using it will save you insane amounts of time. Typing isn't really what it's all about, it's about getting familiar with commands. The command line interface (CLI) will you be frustrating at first but that's okay, everything is frustrating until you master it. First, open up your command line. On Windows, use PowerShell (search for it in the start menu, just don't pick the ISE that's not what we're doing here yet) for Mac, use Finder to get your Terminal running. If you use Linux, this is probably a little beneath you so feel free to skip ahead if you like.

## Some conventions
In this text we will have console input and output. Input will look like this:

```PowerShell
PS Q:\> my-command --with -aflag and text 
```

While output will look like this.
```PowerShell
PS Q:\> my-command --with -aflag and text 
Thanks for using my-command!
```

Sometimes we will just want some inline commands like ```cd myproject``` so context will describe what to do with these.

## Hello World
The first thing we'll do in any language is the cannonical 'Hello World' program so let's get started.
Hopefully that terminal is fired up, here we go:

```PowerShell
PS Q:\> echo 'Hello World'
```
You should see:

```PowerShell
PS Q:\> echo 'Hello world'
Hello world
```