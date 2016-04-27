[![Build Status](https://jenkins.ncrmnt.org/job/GithubCI/job/aura-cli/badge/icon)](https://jenkins.ncrmnt.org/job/GithubCI/job/aura-cli/)

# AURA commandline client

This is a small tool that allows you to call remote aura functions via commandline.

```
AURA Commandline Tool. (c) Necromant 2015
Usage:
       ./auracli -v|--version
       ./auracli -h|--help
       ./auracli -L|--list-transports
       ./auracli -t|--transport=name -o|--option="opts" -l|--listen
       ./auracli -t|--transport=name -o|--option="opts" -c|--call methodname arg1 arg2 ...
```
# Examples

## Calling remote methods

```
0 ✓ necromant @ invyl ~ $ auracli -t dummy -o "blah" -c echo_seq 1 2 3
result:  1  2  3
```

## Listening for events

```
0 ✓ necromant @ invyl ~ $ auracli -t dummy -o "blah" -l
event: ping |  12
event: ping |  12
event: ping |  12
^C
```
