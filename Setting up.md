## Venv
* creating a virtual env to isolate packages you install for the project
* what it is?
	* a directory with some files in it
* Every time you install a **new package** in that environment, **activate** the environment again
### Creating
``` bash
python -m venv .venv
# uses a program called python
# -m call module as a script
# use venv module
# .venv create venv in a new dir .venv

```
### Starting
``` bash
source .venv/bin/activate
```

### Upgrade pip
python -m pip install --upgrade pip

### Add gitignore
to exclude everything from .venv
``` bash
echo "*" > .venv/.gitignore
```
- `echo "*"`: will "print" the text `*` in the terminal (the next part changes that a bit)
- `>`: anything printed to the terminal by the command to the left of `>` should not be printed but instead written to the file that goes to the right of `>`
- `.gitignore`: the name of the file where the text should be written

And `*` for Git means "everything". So, it will ignore everything in the `.venv` directory.


# Managing Dependencies
### requirements
t's a (very) good idea to put the packages and versions your program needs in a file (for example requirements.txt or pyproject.toml).

A requirements.txt with some packages could look like:
``` bash
fastapi[standard]==0.113.0
pydantic==2.8.0
```

We will stick with poetry for now
1) https://python-poetry.org/docs/#installation
2) https://python-poetry.org/docs/basic-usage/
3) I think we can either use our own venv or use poetry , poetry will respect any existing venv but I need to activate it before running any poetry commands that expect to manipulate an environment 