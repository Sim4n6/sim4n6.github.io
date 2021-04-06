---
title: [POC] CLI processor for .bash_history files
updated: 2019-09-27 10:39
---

# Orca
 <img src="https://raw.githubusercontent.com/Sim4n6/Orca/master/orca.png" /> **Orca** a cmdline tool to process .bash_history file using SQLite dbms via SQLAlchemy. 

Code source : <https://github.com/sim4n6/orca>

### Usage :

```
usage: Orca [-h] [-p bash_history] [-e format] [-lc] [-c] [-l] [-s term] [-v]

Process .bash_history file via sqlite3 database.

optional arguments:
  -h, --help            show this help message and exit
  -p bash_history, --process bash_history
                        process a .bash_history file into an sqlite db.
  -e format, --export format
                        export .bash_history content into csv or json.
  -lc, --lastcmd        print the last typed command in bash.
  -c, --count           count the number of items in history.
  -l, --list            list the items of bash history.
  -s term, --search term
                        search for the term in the db.
  -v, --version         print the current script version

Examples: 
    orca.py --process .bash_history_sample1 --count
    orca.py --process .bash_history_sample1 -lc -s "curl" -c
```

