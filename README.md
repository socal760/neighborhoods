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

Depending on whether you're using the command line tools or the GUI, some of these steps will be different.

### Clone

The first step is to copy down our repository. This is called cloning.

```
git clone https://github.com/maptimeLA/neighborhoods.git
```

You should now be able to run a local version of our neighborhood haiku app.

In your terminal change to our *project directory* (this is the folder you just cloned).
```
cd neighborhoods
```

Then use python to start a local webserver.
```
python -m SimpleHTTPServer
```

Now open a browser and go to "localhost:8000". You should see our haiku map. If not, or if you see some kind of error, there was a problem with setup somewhere. Let us know, and we'll help you figure it out!

To quit the local webserver, in the terminal type ctrl+c.

### Edit

The first thing to do when making changes to a project, is to create a new branch. What **is** a branch anyway?

Remember we're writing **place** haikus. So think about the place you want to write about, and create a branch named after that place. 

Since your other terminal is busy serving our website, you'll need a new one. Open another terminal and go to our project directory.

```
cd ~/GitHub/neighborhoods
git checkout -b echo-park-lake-haiku
```

Then open your text editor and use it to open the `haiku.csv` file in our project directory.

Now, come up with a haiku about your place.

**This is the hard part.** Traditional Japanese Haiku are "short poems about a fleeting moment in nature" with no specific syllabic constraints. Less traditionaly, American haiku's tend to follow a rigid three line "5-7-5" syllable format and tend to be about whatever. Either way, don't fret too much. Any issues with your haiku will be addressed in our forthcoming rigourous *haiku pull request* process. :wink: 

**This is the easy part.** We'll need the latitude and longitude of your place to be able to plot it on the map. There are lots of ways to find lat/lon. Try this on: http://itouchmap.com/latlong.html

Once you've decided on a place, found it's lat/lon, and come up with a haiku, enter it into the haiku.csv in a similar format to the existing haiku.

```
github,haiku,latitude,longitude
"michaelkirk","Illicit lotus<br />Chili mango, jicama<br />This lake has secrets.",34.073,-118.261
```

**Note** put your haiku in quotes, and separate the lines with a `<br />` html tag.


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

What's a pull request?

In your browser...

 - Go to https://github.com/maptimeLA/neighborhoods
 - Go to "Pull requests" and then "Create"
 - Leave the base branch as "gh-pages" but change the "compare" branch to your branch name. 

Don't see it? Then likely there was an issue with the [push](#push) step. Try again or ask for some help!

At this point, your pull request is waiting to be merged back into the main project. Try to find a nice reviewer for feedback on your haiku and it will get merged in no time!

If you see an error about *merge conflicts*, ask for help!
