# blibs

Base python libs


```python
from blibs import init_root_logger
init_root_logger(level=10)
```


## Setup dev env

```bash
python3 -m venv venv
. venv/bin/activate
pip install -r requirements-dev.txt
pre-commit install
```

## Test

```bash
. venv/bin/activate
pip install -e .
pytest --cov-report html --cov-report term --cov-report xml:cov.xml
```

## Build

```bash
echo x.y.z > VERSION
pip install -r requirements-release.txt
python -m build -s -w
```
