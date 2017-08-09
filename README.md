# Test of an monolithic repository 

## Installation

### First time only

I am using the following git extension to work with subtrees.
Follow the install instrations [here](https://github.com/dflydev/git-subsplit).


## Initialize your subtrees with subsplit

### 1 - remove existing subsplit configuration directory

`Windows user / powershell`
```powershell
rm -Recurse -Force .\.subsplit\

```

`*ix user / bash`
```bash
rm -rf .subsplit/
```

### 2 - init subsplit

```bash
git subsplit init git@github.com:christian-graf/mono.git
```

## Update subtrees with subsplit

```bash
git subsplit update --heads="master" packages/sub1:git@github.com:christian-graf/sub1.git
```

## Publish subtrees with subsplit

```bash
git subsplit publish --heads="master" packages/sub1:git@github.com:christian-graf/sub1.git
```