# [luvi-builder-samples]

Demonstrates how to use [luvi-builder] by building [luvi]'s application samples. Designed to be used directly from Git it provides a ready-to-fork project to build your own applications with. MIT-licensed, although the [luvi] samples are Apache 2 Licensed.

## Demonstration Quick Start

The application samples are in the `applications` folder.
 
### Firstly, run this snippet to get the code from GitHub

```bash
git clone https://github.com/raphaelcohn/luvi-builder-samples.git
cd luvi-builder-samples
git submodule update --init --recursive
```

### Secondly, build the samples using `./build`.

Output goes in the `release/` folder. Currently this demonstration relies on a copy of [luvi] for your environment, which may not yet exist. The demonstration bundles [luvi] for Mac OS X and Linux x86_64 (amd64).

### Thirdly, run an application sample

Use `./build run -- repl` to run the `repl` application. Hit `CTRL-C` to exit. You can also do more with `./build` - look at its help.

## Build Your Own Applications by bootstrapping from this repository

Remember, applications go in `applications`. Each application has a name - this is a subfolder in `applications` - and a `main.lua` file. Other lua files go next to `main.lua`. See the sample applications for the layout. So, to create your own application `myfirstapp`, do the following:-

1. [Fork me on GitHub](https://github.com/raphaelcohn/luvi-builder-samples/fork)
2. Run the shell snippet above, substituting your forked `.git` URL
3. Then get rid of the samples with `git rm applications/*`
4. Create your application
  1. `mkdir applications/myfirstapp`
  2. `touch applications/myfirstapp/main.lua`
  3. Add some lua to `main.lua`, eg `print "hello world"`
5. Try it out with `./build --run -- myfirstapp`
5. Run `./build`
6. Remember to modify `LICENSE` and `COPYRIGHT` as appropriate, then `git commit` and `git push`
7. You're done!

[luvi-builder-samples]: "https://github.com/raphaelcohn/luvi-builder-samples" "luvi-builder homepage"
[luvi-builder]: "https://github.com/raphaelcohn/luvi-builder" "luvi-builder homepage"
[luvi]: "https://github.com/luvit/luvi" "luvi homepage"
