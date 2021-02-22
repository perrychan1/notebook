## Terminal

| Command | Description |
| :-----: | ----------- |
| `ctl + a` | go ahead of line |
| `ctl + e` | go to end of line |
| `ctl + w` | delete a word |
| `ctl + h` | delete a char |
| `ctl + b` | go back |
| `ctl + f` | go forward |

## Shell

```sh
# os version
# ubuntu
lsb_release -a
# or
cat /etc/*release
# centos
cat /etc/centos-release

# show users, groups
cat /etc/passwd
cat /etc/group

# show network info and ip
ifconfig
```

```sh
# display free disk space
df -h

# display disk usage statistics
du -h --max-depth=1 -x /usr/local/
```
