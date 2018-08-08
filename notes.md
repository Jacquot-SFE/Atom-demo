# Notes for Atom + Git

#### And a peek at VSCode's mirror image of it.

I discovered Atom in a previous position - I was writing a lot of MD for our CMS, and Atom has a native Markdown mode that works offline.

Turns out it's a reasonably capable text editor for general-purpose programming tasks.

## What Is Atom?

It's the Github-sponsored text editor.

[Atom.io](atom.io)

Built on Electron, using Chromium and Node.

### Advantages

* Cross platform.
* Highlight modes for many programming languages.
* Expandable using modules.
    * Some are "core", bundled with the editor, other are community contributed.
    * That's how the language support is built.
* Easy project browsing - just open a folder instead of a file.

### Disadvantages

* Expandable using modules.
    * Some expected features aren't intrinsic.
    * **del** key?  Really
    * Sometimes duplicate or conflicting.
* Modules written in coffee script - not the fastest language.  Still better than Eclipse.

### My History with Git

...it's command line intensive.  

...it's got lots of features for sophisticated use cases, which sometimes get in the way of simple workflows.  Especially if you invoke those features accidentally by fatfingering the command line.


### Git Integration

I stumbled on this unexpectedly.  I was working on getting authentication on a number of repos configured, and clicked on the lower status bar, which opened the git menu.

### In Use

_Open project by opening top directory._

_**The secret for Git integration**: open the top folder of the repo.  If Atom finds the .git there, it'll use it._

It also assumes you've got command line git configured correctly - if auth is broken, Atom won't magically fix it.

You'll know that Git is initialized if you get 3 items in the lower right status bar:
* The branch icon & branch name.
* The push/pull/fetch option.
* The changed (+/-) files indicator.

_Make some changes._

Edit and save some files.

As you accumulate changes, the little "+/- page" icon in the lower corner indicates the number of changed files.

_Staging and Committing_

Click the page icon, it opens Git pane.

The typical workflow will run down this dialog, from top to bottom.

* Unstaged files are at the top.
* Staged files in the middle.
* Commit message below that.
* Git log below that.

Click an unstaged file, it shows the deltas.

This also shows new files.  

(If you're working in an environment that creates intermediate files, you can configure a .gitignore file to keep git from flagging them as new or changed.)

From here, you can stage the whole file,  selectively stage individual changes or lines, or even delete the delta altogether.

If you need bigger context, pressing lowercase `o` will take you to the relevant line in the source.

Once staged, you can click on the staged file, and get a similar delta view, where changes can be unstaged.

To commmit, enter a commit message, press the commmit button.

Finally, to push upstream (or pull from the remote), press the menu bar item with the up & down arrows.

If you're used to using the heavy hammer of `commit -a`, you likely don't gain much from the graphical integration.  I like having the easy review as part of the commit process.

_Branching_

It also does casual branching via the branch indicator in the status bar.

It easily supports two operations:
* Checking out a specific branch - simply pick it from the list.
* Creating a new branch - don't forget to push it upstream.

It doesn't support merging or history...intrinsically.  There are plugins for it...maybe a topic for another day.



### Fast forward to June, 2018

** MSFT to acquire GitHub **

No more indie credibility for using Atom.  It's part of the 800 pound gorilla.

VSCode is conceptually (and operationally) very similar to Atom.    

* Cross platform, tabbed editor with support for many languages.
* Also built on Electron
* Also extensible with JavaScript/TypeScript.

Main editor is the Monaco component, borrowed from VisualStudio.  Supports auto-completion, symbol navigation, etc.

It has Git integration that's similar to Atom's, only the status items are on the lower left corner.

...
