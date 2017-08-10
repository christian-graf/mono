# Test of an monolithic repository with subtrees

## Initialize your subtrees

### Add your sub repositories

```bash
 git subtree add --prefix=packages/sub1 git@github.com:christian-graf/sub1.git master
 git subtree add --prefix=packages/sub2 git@github.com:christian-graf/sub2.git master

 git push
```

## Publish subtrees

```bash
git subtree push --prefix=packages/sub1 git@github.com:christian-graf/sub1.git master
git subtree push --prefix=packages/sub2 git@github.com:christian-graf/sub2.git master
```

## Git extension `subsplit`

While checking how laravel handles its repositories i found some interesting git extension

[Subsplit](https://github.com/dflydev/git-subsplit)

## Links

- [Git-Tools-Subtree-Merging](https://git-scm.com/book/en/v1/Git-Tools-Subtree-Merging)
- [a git subtrees tutorial](https://medium.com/@v/git-subtrees-a-tutorial-6ff568381844)
- [using git subtrees for repository seperation](https://makingsoftware.wordpress.com/2013/02/16/using-git-subtrees-for-repository-separation/)

