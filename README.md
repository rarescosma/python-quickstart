# Python Quickstart

Premise: you know programming but know no (or only a little of) Python.

**Note**: This is for Python 3, *NOT* legacy Python (2.7)

## Introduction

- Python: a slow, statically typed (but checked at runtime) scripting language.
- Sorry for choosing it, here are some steps to make it less painful

## Virtual environments, packages

```bash
mkdir python-quickstart
cd python-quickstart
pyvenv env
source env/bin/activate
```

Packages are pulled from [PyPi](https://pypi.python.org/pypi/pudb) (not to be confused with [PyPy](http://pypy.org/) an alternative to CPython)

```
pip install pudb
pip install pudb==2016.2
pip install pudb>=2016.0
```

```
# requirements.txt
requests==2.13.0
# requirements_dev.txt
-r requirements.txt
pudb==2016.2
# command line:
pip install -r requirements_dev.txt
```

```
pip freeze > requirements_frozen.txt
pip list --outdated --format=columns
```

## Numbers, strings, lists, tuples, dicts, sets

## Ordered dicts, frozensets, named touple, counter

## Testing, TDD

## Function, decorators

* Closures

## Mocking

## Exceptions

## Classes

* Inheritance
* Magic methods

## List/Dict/Set comprehensions

## Generators

## Itertools and more itertools

## Context managers

## Serialization

* JuJ: Just Use Json
* Pickle and YAML are both security risks!

## Static analyzers, coverage

## Debugging

## Logging

## WSGI, Flask

- WSGI: web standard gateway interface
- "WSGI servers": uWSGI, mod_wsgi, etc
- [Flask](http://flask.pocoo.org/): very basic web framework.
- Uses thread-local variables like `flask.request`
- Has an integrated debugger
- Watch out for security! Doesn't even provide CSRF protection by default: http://flask.pocoo.org/snippets/3/
- Probably should be checked for https://www.owasp.org/index.php/Top_10_2013-Top_10

```python
import flask
app = flask.Flask(__name__)


@app.route("/")
def hello():
    return 1 + "Hello World!"


if __name__ == "__main__":
    app.run(debug=True)
```

## Podcasts

* [Talk Python to Me](https://talkpython.fm/)
* [Podcast.\_\_init\_\_](https://pythonpodcast.com/)
* [Python Bytes](https://pythonbytes.fm/)
