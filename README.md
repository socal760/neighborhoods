# Neighborhood Haiku Map

Tonight we'll be building a map of place-haikus about *your* neighborhood. See the live version here: http://maptimela.github.io/neighborhoods/ 

It's pretty lonely at the moment. We need you to help add haikus to the map! To do this we'll show you how to create a GitHub pull request with your haikus.

## Setup

First a bit of setup...

 - **Create a GitHub account** if you don’t already have one here: https://github.com/
 - **Install git** (either the graphical tool or the command line tool)
   - Graphical tool: https://desktop.github.com/
   - Command line tool: https://help.github.com/articles/set-up-git/#setting-up-git
 - **Install python** (windows only - Mac comes preinstalled) We use python to
serve up our site locally, so you can test your changes.
   - Download Python 3.5 (or any version is fine) here: https://www.python.org/downloads/
   - Detailed installation instructions: http://www.howtogeek.com/197947/how-to-install-python-on-windows
- **Install a text editor.** We use a text editor to write code. There are a
million to choose from. If you’re not sure which one to use, why not
give Atom a try: https://atom.io/

If you get hung up on any of the setup steps *DON’T PANIC!* We can help
you!

## Exercise

The steps are the same, but your methods will vary a bit depending on wether you're using the command line tools or the GitHub GUI.

### Clone

```
git clone https://github.com/maptimeLA/neighborhoods.git
```

### Edit

The first thing to do when making changes to a project, is to create a new branch. What **is** a branch anyway?

```
git checkout -b echo-park-lake-haiku
```

Then open the haiku.csv file in your favorite text editor and add your haiku in a similar format to the others.

```
github,haiku,latitude,longitude
"michaelkirk","Illicit lotus<br />Chili mango, jicama<br />This lake has secrets.",34.073,-118.261
```

Make sure to put your haiku in quotes, and separate the lines with a `<br />` html tag.


### Commit

```
git add haiku.csv
git commit -m "Added my haiku"
```

### Push

```
git push origin echo-park-lake-haiku
```

### Pull request

In your browser go to https://github.com/maptimeLA/neighborhoods
Go to "Pull requests" and then "Create"
Leave the base branch as "gh-pages" but change the "compare" branch to your branch name. Don't see it? Then likely there was an issue with the [push](#push) step. Try again or ask for some help!
