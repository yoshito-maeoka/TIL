# Shell Script

## xargs

### 1. call command with each entry
```
..... | xargs -n 1 ...
```

### 2. call with placeholder

```
.... | xargs -ITOREPLACE command TOREPLACE something-other-part
```

### example use case with both option:
display all files and committer from result of grep
```
grep -r '!important' vue-frontend/src/ | sed -e 's/:.*$//g' | uniq | xargs -n 1 -I{} git log --name-only --pretty='%C(cyan)%cn' -n 1  {}
```
