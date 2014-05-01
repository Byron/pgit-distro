The pgit distribution allows to run pgit without requiring root permissions, both on posix platforms and on windows. It comes with all python dependencies, and need nothing more than a python interpreter to run.

In it's current state, it will help you with managing git-submodules.

## Requirements

* python 2.6 or above
    - currently, python 2.7 is configured to be used
    - interpreter must be configured to be able to launch executable python files
* git 1.7 or newer
    - to checkout repositories

## Installation

All you have to do is to clone this repository, and update all submodules as follows:

```bash
git clone https://github.com/Byron/pgit-distro
cd pgit-distro
git submodule update --init --recursive
```

## Usage

As pgit is a commandline utility, you will need a terminal to control it. 
Here are a few examples

```bash

# Display information about all available subcommands
./bin/pgit -h

# list all submodules in the repository at the current working directory
./bin/pgit submodule query

# call pgit, but use python 2.6 (assuming it is installed in one of the standard locations)
./bin/pgit submodule query ---packages.python.version=2.6

# Learn about everything pgit submodule can do
./bin/pgit submodule -h
```

## License

All files contains in this repository are [MIT licensed](http://opensource.org/licenses/MIT).

## More Information ...

... about pgit's capabilities can be found in the [repository of the package itself](https://github.com/Byron/pgit)
