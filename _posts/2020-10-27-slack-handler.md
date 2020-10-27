---
title: Slack handler 
updated: 2020-10-27 23:37
---

 Slack handler is a python tool to dump file slacks in raw format and to extract file slack information to CSV format. 
 
 More details : <https://github.com/Sim4n6/Slack_handler>
 
 
```
usage: main.py [-h] [-e ENCODING] [-t TYPE] [-p] [-d] [-c CSV] [-v] image

Handle the file slack spaces.

positional arguments:
  image

optional arguments:
  -h, --help            show this help message and exit
  -e ENCODING, --encoding ENCODING Display slack space in LATIN-1 or Hex. Supported options 'latin-1', 'hex'.
  -t TYPE, --type TYPE  Type of image. Currently supported options 'raw', 'ewf'.
  -p, --pprint          Pretty printing of all file slack spaces found.
  -d, --dump            Dump file slack spaces of each file in raw format.
  -c CSV, --csv CSV     Write file slacks information to a CSV file.
  -v, --version         show program's version number and exit
```
