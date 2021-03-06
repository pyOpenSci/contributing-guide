# Testing your package

Testing allows you to be sure that your package behaves the way it is expected
to behave. It also allows you to account for various edge cases that may break
your package's functionality.

For a good introduction to testing, see
[this Software Carpentry lecture](https://swcarpentry.github.io/python-novice-inflammation/10-defensive/index.html)

## What testing infrastructure should I use?

The most common testing tool used in the Python ecosystem is
[the pytest package](https://docs.pytest.org/en/latest/). We recommend using
Pytest to set up testing infrastructure for your package. Pytest also has
a number of extensions that can be used in addition to pytest's core functionality.
Here are a few useful ones:

* [pytest-regressions](https://pypi.org/project/pytest-regressions/) allows you to
  determine whether the contents of a file or data structure change from one build
  to another.
* [pytest-cov](https://pytest-cov.readthedocs.io/en/latest/) allows you to analyze
  the code coverage of your package during your tests, and generates a report that you
  can [upload to codecov](https://codecov.io/).

## Code coverage

Code coverage is the amount of your package's codebase that is run as a part of
running your project's tests. A good rule of thumb is to ensure that **every line of
your code is run at least once during testing**. However, note that good code coverage
does not *guarantee* that your package is well-tested. For example, you may run all of
your lines of code, but not account for many edge-cases that users may have. Ultimately,
you should think carefully about the way your package will be used, and decide whether
your tests adequately cover all of that usage.

A common service for analyzing code coverage is [codecov.io](https://codecov.io/). This
project is free for open source tools, and will provide dashboards that tell you how
much of your codebase is covered during your tests. We recommend setting up an account,
and using codecov to keep track of your code coverage.
