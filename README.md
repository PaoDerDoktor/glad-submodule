# `glad-submodule`, a quickly-submodulable git repo for [glad 2](https://gen.glad.sh)

## What am I looking at ?

This is a small repo intended to be used as a submodule, in order to consider glad as not part of the project you're building as a submodule of it's (thus nor counting the gargantous glad files in your stats). It also helps when you don't really want to go through the glad generator for the *6184318646135th* time.

## Which glad did you generate ?

I generated the files here with the glad2 generator, using those options :

- OpenGL version 4.6 Core
- Vulkan version 1.3
- Only every ARB extensions

It may change in the future, so beware of other commits if you want to submodule other parameters I might have selected before !

If I do things right, a **permalink** to the glad generation I currently use in this repo should be on the [`permalink.txt`](./permalink.txt) file.

## How can I add it in a C/C++ project ?

This repo works with CMake and git. In the next line, we'll consider "`[glad-submodule-path]`" as a placeholder for the path you chose to put this repo in.

First, add it as a git submodule with a command such as `git submodule add https://github.com/PaoDerDoktor/glad-submodule`.

Then, in your `CmakeLists.txt`, simply add the line `ADD_SUBDIRECTORY([glad-submodule-path])`. This will *"import"* two libraries in your file :

- `glad-opengl`
- `glad-vulkan`

Now you just have to choose the one you need and link it to your executable's target !

## Can I contribute ?

Absolutely ! If you think my CMakeLists is wrong, or that I forgot some important extension, or that I missed a Vulkan or OpenGL version change, make a pull request !

## Credits

Glad is absolutely not made by me. Credit goes to [dav1de](https://dav1d.de) !
