# circleci-orb-bits-python

[![CircleCI](https://circleci.com/gh/broadinstitute/circleci-orb-bits-python/tree/master.svg?style=svg)](https://circleci.com/gh/broadinstitute/circleci-orb-bits-python/tree/master)

An orb containing useful [Python][1] commands and jobs for doing CI/CD in [CircleCI][2].  All installs and command runs are assumed to be done with [Pipenv][3] using this orb.

## Commands provided

* **codecov**: Send the coverage report back to [Codecov][5]
* **init-pypi**: Initialize the .pypirc file
* **lint**: Run all linters (YAMLlint and pylama)
* **pkgtest**: Run a test module install using setup.py
* **prereq**: Install and cache dependencies
* **publish**: Publish the module to PyPi
* **unit-tests**: Run Python tests using [green][4]
* **verify-tag**: Verify the internal version vs. the git tag

## Jobs provided

* **preflight**: Run all lint checks
* **run-tests**: Run unit tests, packaging tests, and return coverage report to [Codecov][5]
* **deploy**: Verify the version and then publish a new version to [PyPi][6].

## pre-commit hooks

A configuration is provided for doing pre-commit hook checks using [pre-commit][7].  For all the checks to work you will need to have the following installed already:

* [https://github.com/adrienverge/yamllint](yamllint)
* [CircleCI][2] command-line utility: [https://circleci.com/docs/2.0/local-cli/](circleci)

[1]: https://www.python.org/ "Python"
[2]: https://circleci.com/ "CircleCI"
[3]: https://pipenv.readthedocs.io/en/latest/ "Pipenv"
[4]: https://github.com/CleanCut/green "green"
[5]: https://codecov.io/ "Codecov"
[6]: https://pypi.org/ "PyPi"
[7]: https://pre-commit.com/ "pre-commit"
