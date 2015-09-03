Workaround to Use Conda Environment Instead of pyvenv

-   Inside your project directory...

```bash
rm -rf .venv
mkdir -p .venv/bin
cat > .venv/bin/activate <<EOF
#!/usr/bin/env bash

source $HOME/miniconda/bin/activate py3  # if the name of the env is py3

deactivate() {
    source $HOME/miniconda/bin/deactivate
    unset VIRTUAL_ENV
}

export VIRTUAL_ENV=$CONDA_ENV_PATH
EOF

ln -s $HOME/miniconda/env/py3/python3.4 .venv/bin/python3.4
ln -s $HOME/miniconda/env/py3/python3.4 .venv/bin/python3

```

Now, when you run your makefile, the python binaries are right where you expect
them _and_ `source .venv/bin/activate` will work the same as for a pyvenv.
