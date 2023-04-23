---
title: "Git Submodules"
date: 2023-04-23T15:49:59-04:00
draft: false
---

# My Trial-and-error series 1

git submodules isn't something I use all the time; recently I have to do this when I play with hugo themes.  Here is a step that worked for me

## How to remove git submodules properly

### 1. deinit the submodule

```
$ git submodule deinit <submodule_directory>
```



### 2. remove the submodule directory from git

```
$ git rm <submodule_directory>
```



### 3. remove the submodule directory from .git/modules

```
$ rm -rf .git/modules/<submodule_directory>
```





After this is done, you can commit the changes and push

```
git commit -m"messsage...."
git push
```





#### Reference

[1]: https://anjanashankar.com/2021/05/19/git-submodules/	"a blog from Anjana Shankar"
