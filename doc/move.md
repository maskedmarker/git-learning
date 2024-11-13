# 移动文件或目录

git mv命令在调整文件/目录位置时,同时记录位置转移的细节,不会让转移后的文件丢失历史commit.

## synopsis
```
git mv [-v] [-f] [-n] [-k] <source> <destination>
git mv [-v] [-f] [-n] [-k] <source> ... <destination-directory>
```

In the first form, it renames <source>, which must exist and be either a file, symlink or directory, to <destination>. 
In the second form, the last argument has to be an existing directory; the given sources will be moved into this directory.
The index is updated after successful completion, but the change must still be committed.

## 注意:
1. idea在重构的过程中,如果碰到调整类的包名,可能会用git的rm+add来替换git的mv命令,从而丢失文件的历史commit.