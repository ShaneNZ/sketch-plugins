# sketch-plugins
All the plugins I use regularly, in one repo, for easy updating.

**Note:** this repo probably isn't really that useful to you directly, but how it works might be if you have the same problem I do. 

## Why have you done this?
Because Sketch Toolbox doesn't update plugins any more, and I'm tired of doing it manually. I want to do one "check for updates" thing every so often, and have it magically happen for me.

## So how does this work?
Each plugin I use is added to this repo as a submodule. This approach isn't intended for working on the individual plugins ( there's probably a way of doing that, it's just not something I'm doing at the moment).

To kick it off, open the Sketch plugins directory and then:

    git clone --recursive https://github.com/shanenz/sketch-plugins.git'
    
This will give you sketch-plugins folder with all the plugin/submodules in it. This just keeps your "managed" plugins apart from any other plugins you might install by double clicking on them or whatever. It doesn't affect how they're used in Sketch.

To add a new plugin to the list, **make sure you're in the sketch-plugins folder:**

    git submodule add https://github.com/design4use/gb-sketch-segmentcircle "added segmentcircle" 

To update all your plugins:

    git submodule foreach --recursive git pull origin master

Remember that you need to commit and push once you've added a plugin or updated.

For more info, see https://git-scm.com/book/en/v2/Git-Tools-Submodules. If you're not keen on the commandline, then GitKraken nicely handles submodules - give that a go.

## Excluded plugins
I also use the following plugins, but they have their own update mechanism built in, so they're not in the repo:
- Sketch Runner
- Craft
- Sketch Measure

Plugins that don't have a Github repo:
- Send to Flinto

### Disclaimer
There's probably a better way to do it, but I'm no Github expert. This way works but if there's a better way, then please let me know :)
