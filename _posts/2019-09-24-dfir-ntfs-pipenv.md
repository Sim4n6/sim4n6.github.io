---
title: Installation of dfir_ntfs pkg from Github on a virtual env using Pipenv
update: 2019-09-24 12:12
---

```python
# start a virtual environment
pipenv shell

# define python 3.7 as the used version
pipenv --python 3.7

# install the dependencies
pipenv install setuptools

# install the pkg dfir_ntfs from the VCS 
pipenv install -e git+https://github.com/msuhanov/dfir_ntfs.git#egg=dfir_ntfs
```

and that's it.
