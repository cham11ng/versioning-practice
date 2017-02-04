## Git Basics - Tagging

### Tagging
Git uses two main types of tags: lightweight and annotated.

* A lightweight tag is very much like a branch that doesn’t change – it’s just a pointer to a specific commit. 
* _It’s generally recommended that you create annotated tags_ so you can have informations.

### Lightweight Tags

If you want a temporary tag or for some reason don’t want to keep the other information.

```shell
$ git tag v1.4.1

$ git show v1.4.1
tag v1.4.1
Tagger: Sagar Chamling <sgr.raee@gmail.com>
Date:   Sat May 3 20:19:12 2016 -0700
```

### Annotated Tags

Annotated tags, however, are stored as full objects in the Git database. They’re checksummed; contain the tagger name, email, and date; have a tagging message; and can be signed and verified with GNU Privacy Guard (GPG)

```shell
$ git tag -a v1.4.1 -m "Version 1.4.1"

$ git show v1.4.1
commit ca82a6dff817ec66f44342007202690a93763949
Author: Sagar Chamling <sgr.raee@gmail.com>
Date:   Mon Mar 17 21:52:11 2016 -0700
```

### Tagging Procedure

```shell
$ touch README.md
$ touch .gitignore
$ touch LICENSE.md

$ git add .

$ git commit -m "Initial Commit. README, LICENSE, .gitignore file created."

$ git remote add origin git@github.com:cham11ng/versioning_practice.git

$ git tag -a v1.0.0 -m "Version 1.0.0"

$ git push -u origin master --tags
```
## References
* https://git-scm.com/book/en/v2/Git-Basics-Tagging