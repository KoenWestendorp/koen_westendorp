---
layout: post
title: My Personal Guide to Git
cover-image: /img/blog/image3.jpg
---

This is my Personal Guide to Git (or PGG for short).
## Basic commands
First you want to check in on the *git status* of your project.

``bash
git status
```

## Setting up
The first thing to do when setting up git is initializing git.

``bash
git init
```

*…thats it!*

Then its smart to check the status of your project.

``bash
git status
```

You most likely want to publish your stuff on [GitHub](https://github.com). To make that magic happen you need to set a *remote name* and *repository url*. You will most of the time call it *origin*.

```bash
git remote add origin https://github.com/KoenWestendorp/some-repo-name.git
```


## Adding, committing and pushing
Off course you want to make the changes you make to your project to become part of the timeline of the [branch](#branches) you’re on. First you need to *add* the changes.

```bash
git add .
```

*The dot basically means “everything that changed”. You can also make it to add certain files, filetypes or folders.*

To *commit* the things you *added* onto a branch you can use this command:

```bash
git commit -m "Added 🍋🍊 and 🍦🍨🍰"
```

To *add* **and** *commit* at the same time you can use this line of text:

```bash
git commit -a -m "Added 🐺, 🐦🐧🐔 and 🍫🍭"
```

After *addin’* ’n *commitin’* you can start *pushin’*.

```bash
git push origin master
```

*Origin being the remote version of your repo and master being the branch you’re on in this situation.*


## Logging and checking
It is always a good idea to check in on the status of your project every once in a while. You can view the status of git in your project by typing:

```bash
git status
```

as discussed earlier.
To see a list of different iterations in your project you can use:

```bash
git log
```

This show a list of the changes made over time but is pretty messy. Thats the reason I use this command most of the time:

```bash
git log --oneline --graph
```

*Because of the `--oneline` option it is just one line instead of 5 (!) and if you’re not working with other people or don’t need to see what day and time it was committed it sure is enough.*
