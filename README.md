# sample-module

__Baseline Sample Module__; template using TOML config and backup to setup.cfg which is due to be retired eventually as well as setup.py is no longer recommended, but sometimes required for backport as TOML has features still in *beta*.

## Background

__[PEP 518](https://www.python.org/dev/peps/pep-0518/#sticking-with-setup-cfg)__, first drafted in 2016, was marked as final in April of 2020. I'm interpreting it as an invitation to use pyproject.toml instead of setup.cfg. Quoting from the PEP:

>There are two issues with setup.cfg used by __setuptools__ as a general format. One is that they are __.ini__ files which have issues as mentioned in the [configparser](https://docs.python.org/3/library/configparser.html#module-configparser) discussion above. The other is that the schema for that file has never been rigorously defined and thus it's unknown which format would be safe to use going forward without potentially confusing setuptools installations.

__From [black's documentation](https://black.readthedocs.io/en/stable/usage_and_configuration/the_basics.html#what-on-earth-is-a-pyproject-toml-file):__

> __[PEP 518](https://www.python.org/dev/peps/pep-0518/)__ defines __pyproject.toml__ as a configuration file to store build system requirements for Python projects. With the help of tools like [Poetry](https://poetry.eustace.io/) or [Flit](https://flit.readthedocs.io/en/latest/) it can fully replace the need for __setup.py__ and __setup.cfg__ files.

[pip 19.0](https://github.com/pypa/pip/blob/main/NEWS.rst#190-2019-01-22) (2019-01-22) implemented [PEP 517](https://www.python.org/dev/peps/pep-0517/) to allow projects to specify a build backend via __pyproject.toml__.

[PEP 621](https://peps.python.org/pep-0621/) which specifies a a standard way of storing project metadata in pyproject.toml, was marked as final on March 3, 2021.

setuptools has an open issue titled "[Eventually deprecate __setup.cfg__ with automatic conversion to pyproject.tom](https://github.com/pypa/setuptools/issues/3214)l".

__Disclaimer:__ see [stakflow post](https://stackoverflow.com/questions/44878600/is-setup-cfg-deprecated).

__Recommended further reading:__ [Why you shouldn't invoke setup.py directly](https://blog.ganssle.io/articles/2021/10/setup-py-deprecated.html) by Paul Ganssle.
