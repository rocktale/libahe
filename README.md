# libahe
A collection of little bash helpers.

## py3venv
Functions for virtual environments created by the python3
[venv](https://docs.python.org/3/library/venv.html) module.
This is a very tiny imitation of my most used functionality of tools such as
[virtualenvwrapper](https://virtualenvwrapper.readthedocs.io): Starting to work
in a given environment with a very short command - including autocomplete for
the available environments.

Simply load the functions from `py3venv`:

```
source libahe/py3venv
```

You can put this in your `.bashrc` or whatever script you use to setup your bash.
The helper provides a single command - `workon` - which can do two things:

1. If followed by the name of a virtual environment, it activates it, e.g.
`workon conan`

2. If the option `-c` is added in front of the environment name, it is created
before activation if it does not exist already, e.g. `workon -c nikola`

The following variables can be set to fine tune the behavior:

- **PYVENV_WORKON_HOME**: Variable defining the base directory of all virtual
environments; defaults to `~/.pyvenv`
