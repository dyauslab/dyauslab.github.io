---
title: "Dev&Ops Series 1 - Git Submodules"
type: post
date: 2023-04-23T15:49:59-04:00
draft: false
summary: "How to remove a git submodules"
---

Git submodules can be a powerful tool in managing dependencies within a Git repository, but they can also be a bit tricky to work with. As someone who doesn't use them frequently, I recently found myself needing to use them when playing around with Hugo themes. Through some trial and error, I discovered a simple yet effective method that worked for me. In this blog post, I will share my experience and provide step-by-step instructions to help you successfully work with Git submodules in your own projects.


## How to remove git submodules properly

### 1. deinit the submodule

```bash
$ git submodule deinit <submodule_directory>
```

### 2. remove the submodule directory from git

```bash
$ git rm <submodule_directory>
```

### 3. remove the submodule directory from .git/modules

```bash
$ rm -rf .git/modules/<submodule_directory>
```

### After this is done, you can commit the changes and push

```bash
git commit -m"messsage...."
git push
```

### Reference:
https://anjanashankar.com/2021/05/19/git-submodules/
