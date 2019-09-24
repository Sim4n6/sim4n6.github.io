---
title: How to install dfir_ntfs from Github using Pipenv
update: 2019-09-24 12:12
---

```
pipenv shell
pipenv --python 3.7
pipenv install setuptools
pipenv install -e git+https://github.com/msuhanov/dfir_ntfs.git#egg=dfir_ntfs
```

and that's it.
