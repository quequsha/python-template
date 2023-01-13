# python-template

A [`python`](https://www.python.org) template that provided default [`pre-commit`](https://github.com/pre-commit/pre-commit) and [`pip-compile-multi`](https://github.com/peterdemin/pip-compile-multi) features.


## How to install template for development?

1. Install [`cookiecutter`](https://github.com/cookiecutter/cookiecutter) at your environment:
```
$ pip install cookiecutter
```
2. Load structure:
```
$ cookiecutter gh:quequsha/python-template
```
3. Install `development` dependicies:
```
$ pip install -Ur requirements/dev.txt
```
4. Init git if needed:
```
$ git init
```
5. Add remote repo if needed:
```
$ git remote add origin <repo>
```
6. Init `pre-commit`:
```
$ pre-commit
```
7. Install `pre-commit` hooks:
```
$ pre-commit install
```

## How to use template?

> Each core dependency add to `requirements/base.in`

> Before commit run `pip-compile-multi`

> After `git commit ...` will call `pre-commit` check automatically.

> At production you should only install dependicies: `pip install -Ur requirements/base.txt`


## Additional hooks
Your can add another `pre-commit` hooks to `.pre-commit-config.yaml`
Explore:
- [supported hooks](https://pre-commit.com/hooks.html)
- [pre-commit-hooks](https://github.com/pre-commit/pre-commit-hooks)
- [awesome-flake8-extensions](https://github.com/DmytroLitvinov/awesome-flake8-extensions)

## Development packages
- [pytest](https://docs.pytest.org/)
- [pysnooper](https://github.com/cool-RR/PySnooper)
- [py-spy](https://github.com/benfred/py-spy)
- [memray](https://github.com/bloomberg/memray)

## Useful commands
Run commit without `pre-commit`:
```
$ git commit --no-verify
```
Run `pre-commit` against all the files:
```
$ pre-commit run --all-files
```
Configure dependicies:
```
$ pip-compile-multi
```
