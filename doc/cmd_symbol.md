# git命令中特殊符号

The -- is a safety mechanism in Git to eliminate ambiguity and ensure Git correctly interprets file paths. 
It’s particularly useful when a file name could be mistaken for a branch or commit hash.

For example:
```bash
git diff branch1..branch2 -- path/to/file
```

Here, -- tells Git that path/to/file is a file or directory, and not a branch or other reference. 
This is especially useful if the file name could be confused with a branch or a commit hash.



