# [alpha] menpotoolkit

### What is menpotoolkit?
menpotoolkit is a single directory that you can download which contains 
the latest stable version of The Menpo Project. Download and unpack one
zip file, and you immediately have access to:

1. A full isolated Python installation containing all of menpo and its depenencies
2. A set of notebooks that you can run immediatly to see how to use menpo
3. A set of command line tools, `menpofit`, and `menpodetect`, that can be used to locate bounding boxes and landmarks in challenging in-the-wild facial images.

There is no installation step, you just run executables in the downloaded folder.
To remove, simply delete the folder.

### Who is menpotoolkit for?

menpotoolkit is ideal for people who are completely new to Python and are
interested to try out Menpo, perhaps for it's command line tools and
useful prebuilt facial models. It replicates the experience of downloading a 
traditional piece of software, running `make`, and having a bunch of 'executables' ready 
to play with. Only, you don't need to run `make`. :)

It's also useful for more advanced users as a convenient method to generate a
clean install of the latest stable version of menpo that is not only unrelated
to the system Python, but even unrelated to any existing conda installation.
menpotoolkit essentially runs the same bootstrapping script we use when
performing Continuous Integration (CI) testing, so if you are worried you have
in any way borked your existing menpo installation, it can be convenient to
download menpotoolkit to get a clean slate to test something out in.

### Wait, so is this the preferred way to install Menpo?

If you don't have a clue about Python and want to play with Menpo as soon as
possible, yes. If you are a experienced Python user, **no**. You should just
use conda as normal and conda install menpo.

### Why would I not just use this though? What's the benefit of having a proper conda installation?

Once you have been using Python a little you will realize that the structure of
conda (or virtualenv) where you have multiple isolated environments that can be
easily switched between is really valuable. You'll also want all those utilities
to be on your path at all times, so you don't have to live out of one folder on
your system like a hermit. Then you'll get to grips with installing development
versions of packages so you can edit them to contribute back to the community.
You'll discover git and it will transform the way you conduct your work or
research.

One day all this will make sense and you will want to maintain a global conda
install to make your life easier. Until then, menpotoolkit is here.

### Why are you making another mechanism for Python installation? Isn't it confusing enough as it is?

menpotoolkit is **not a new way to install a general Python installation**. 
We aren't reinventing the wheel (tehe) here.
If you are already experienced with Python then feel free to `conda install
-c menpo menpoproject` and be glad that we have built all our binary dependencies so everything
just works on Linux Windows and OS X. If you really want to `pip install menpo`
you can, but you'll have a real fight on your hands to get all our binary
dependencies intalled. (Seriously, don't fight it, just use conda).

Our project unfortunately lies at the interaction of having very
challenging dependencies to install (hence our insistence on conda) and
appealing to people who may be completely new to the Python community.
A researcher who has solely used Matlab for 20 years is going to understandably
be intimidated by having to setup a 'correct' Python environment to just try and
call `menpofit`'s assortment of excellent face alignment techniques.
menpotoolkit lowers the barrier to entry considerably so we can welcome in such
users. Maybe they will see the light and embark upon learning about how to use
Python correctly - that's great, one day they won't need menpotoolkit any more.

### Can I move the menpotoolkit folder?

Sure, put it where you like.

### Can I put my .py files and notebooks inside it?

No. Don't place anything inside `./menpotoolkit`. You may want to blow this away
in the future - keep your own code elsewhere.


### Can I upgrade to newer versions of Menpo?

Sure, just run `./menpotoolkit/upgrade`


### Can I use development versions of Menpo?

No. Well, you can, but we aren't encouraging that. If you want to use
development builds of Menpo then you really should be managing a proper conda
installation.

### Can I install other Python packages?

Sure. First try `./menpotoolkit/conda install PACKAGENAME`. If that fails, go for
`./menpotoolkit/pip install PACKAGENAME`

### Wait, I screwed something up trying to install other packages. How do I reset menpotoolkit?

Just delete the folder, download a fresh copy, and unpack. :)
