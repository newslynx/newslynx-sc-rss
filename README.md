[![Build status](https://travis-ci.org/newslynx/newslynx-sc-rss.svg)](https://travis-ci.org/newslynx/newslynx-sc-rss) [![Documentation Status](https://readthedocs.org/projects/newslynx-sc-rss/badge/?version=latest)](https://readthedocs.org/projects/newslynx-sc-rss/?badge=latest)

newslynx-sc-rss
==========================================================================================



## Installation

### Production

To install `newslynx-sc-rss` for an active installation of `newslynx-core`, clone it and copy into `~/.newslynx/sous-chefs`

```bash
$ git clone https://github.com/newslynx/newslynx-sc-rss.git
$ mv newslynx-sc-rss/ ~/.newslynx/sous-chefs/
```

Now install it within the same virtual environment as `newslynx`:

```bash
$ cd ~/.newslynx/sous-chefs/newslynx-sc-rss/
$ pip install .
```

... and if you're running `newslynx` as `sudo`


```bash
$ cd ~/.newslynx/sous-chefs/newslynx-sc-rss/ 
$ sudo pip install .
```

Finally, run `newslynx sc-sync` to `newslynx-sc-rss`'s Sous Chefs for all organizations.

```bash
$ newslynx sc-sync
```

### Development 

If you want to modify / add Sous Chefs to `newslynx-sc-rss`, instal it in it's own virtual environment.

**NOTE** Will install a fresh version of `newslynx` via `pip`.

```bash
$ mkvirtualenv newslynx-sc-rss
$ git clone https://github.com/newslynx/newslynx-sc-rss.git
$ cd newslynx-sc-rss
$ pip install --editable .
```

You should now be able to run `newslynx-sc-rss`'s Sous Chefs in development mode

```bash 
% newslynx sc newslynx_sc_rss/say_my_name.yaml --myname='Brian Abelson'
```

## Tests

Requires `nose`

```bash
$ make all_tests
```

## Documentation

Documentation for `newslynx-sc-rss` is hosted on [Read The Docs](http://newslynx-sc-rss.readthedocs.org/).

It's generated via the following steps

* converts this file (`README.md`) into a ReStructured Text file, saving it to [docs/index.rst](https://github.com/newslynx/newslynx-sc-rss/blob/master/docs/index.rst)
* runs `newslynx sc-docs newslynx_sc_rss -f rst` to generate documentation for all the Sous Chefs in `newslynx-sc-rss` and saves the output to [docs/sous-chefs.rst](https://github.com/newslynx/newslynx-sc-rss/blob/master/docs/sous-chefs.rst)
* Builds Sphinx Documentation from these files.


## Continuous Integration

Builds for `newslynx-sc-rss` can be found on [Travis](https://travis-ci.org/newslynx/newslynx-sc-rss)

## Contributing

See the [contributing guidelines](https://github.com/newslynx/newslynx-sc-rss/blob/master/CONTRIBUTING.md).


## What's in this module ?

- [README.md](https://github.com/newslynx/newslynx-sc-rss/blob/master/README.md)
	* This file 

- [VERSION](https://github.com/newslynx/newslynx-sc-rss/blob/master/VERSION)
	* `newslynx-sc-rss`'s source-of-truth version.

- [requirements.txt](https://github.com/newslynx/newslynx-sc-rss/blob/master/requirements.txt)
	* `newslynx-sc-rss`'s python dependencies.

- [MANIFEST.in](https://github.com/newslynx/newslynx-sc-rss/blob/master/MANIFEST.in)
	* Specifications for which files to include in the PyPI distribution.
	* See the docs on this [here](https://docs.python.org/2/distutils/sourcedist.html#specifying-the-files-to-distribute).

- [setup.py](https://github.com/newslynx/newslynx-sc-rss/blob/master/setup.py)
	* Specification's for building `newslynx-sc-rss`'s PyPI distribution.

- [.travis.yml](https://github.com/newslynx/newslynx-sc-rss/blob/master/.travis.yml)
	* Configurations for Travis Continuous Integration
	* You must activate this project on [travis-ci.org](https://github.com/newslynx/newslynx-sc-rss/blob/master/http://travis-ci.org/) for this to run on subsequent updates.

- [Makefile](https://github.com/newslynx/newslynx-sc-rss/blob/master/Makefile)
	* Helpers for managing `newslynx-sc-rss`.
	* Includes:
		- `make clean`: 
			* Cleans out cruft from this directory.
		- `make install`: 
			* Installs `newslynx-sc-rss`. Assumes that you're in a virtual environment.
		- `make all_tests`: 
			* Runs the tests.
		- `make readme`
			* Converts this file to `.rst`, including a table of contents, and saves it to [docs/index.rst](https://github.com/newslynx/newslynx-sc-rss/blob/master/docs/index.rst)
		- `make sous_chef_docs`
			* Programmtically generates [Sous Chef documentation](https://github.com/newslynx/newslynx-sc-rss/blob/master/docs/sous-chefs.rst) by running `newslynx sc-docs newslynx_sc_rss/ --format=rst > docs/sous-chefs.rst`.
		- `make all_docs`: 
			* Builds the sphinx docs for `newslynx-sc-rss` by running the above two commands.
		- `make view_docs`
			* Serves documentation at [localhost:8000](http://localhost:8000)
		- `make register`: 
			* Registers `newslynx-sc-rss` on [PyPI](https://pypi.python.org/pypi).
		- `make distribute`: 
			* Publishes a new version of `newslynx-sc-rss` to PyPI.

- [CONTRIBUTING.md](https://github.com/newslynx/newslynx-sc-rss/blob/master/CONTRIBUTING.md)

- [newslynx_sc_rss](https://github.com/newslynx/newslynx-sc-rss/blob/master/newslynx_sc_rss/)
	* `newslynx-sc-rss`'s source code and Sous Chef configuration files.

- [docs](https://github.com/newslynx/newslynx-sc-rss/blob/master/docs/)
	* Sphnix documentation for `newslynx-sc-rss`

- [tests](https://github.com/newslynx/newslynx-sc-rss/blob/master/tests/)
	* `nose` tests for `newslynx-sc-rss`

