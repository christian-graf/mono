# Test of an monolithic repository 

## Installation

### First time only

I am using the following git extension to work with subtrees.
Follow the install instrations [here](https://github.com/dflydev/git-subsplit).


## Initialize your subtrees with subsplit

### Add your sub repositories

```bash
 git subtree add --prefix=packages/sub1 git@github.com:christian-graf/sub1.git master
 git subtree add --prefix=packages/sub2 git@github.com:christian-graf/sub2.git master

 git push
```

### Remove existing subsplit configuration directory

`Windows user / powershell`
```powershell
rm -Recurse -Force .\.subsplit\

```

`*ix user / bash`
```bash
rm -rf .subsplit/
```

### Init subsplit

```bash
git subsplit init git@github.com:christian-graf/mono.git
```

## Update subtrees with subsplit

```bash
git subsplit update
```

## Publish subtrees with subsplit

```bash
git subsplit publish --heads="master" --no-tags packages/sub1:git@github.com:christian-graf/sub1.git
git subsplit publish --heads="master" --no-tags packages/sub2:git@github.com:christian-graf/sub2.git
```