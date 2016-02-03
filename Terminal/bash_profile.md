# .Bash_profile: сделать  bash promt чуть удобнее
## Больше цвета
**Вывод:**
``` $ export CLICOLOR=1 ```
``` $ export LSCOLORS=ExFxBxDxCxegedabagacad ```
**GIT:**
``` $ git config --global color.ui true ```
## Больше информации
```
$ export PS1="\[\033[36m\]\u\[\033[m\]@\[\033[32m\] \[\033[33;1m\]\w\[\033[m\] (\$(git branch 2>/dev/null | grep '^*' | colrm 1 2)) \$  \n| => "
$ export PS2="| => "
```
сделает
```
username@**~/current_path** (branch) $
| => ...
```

