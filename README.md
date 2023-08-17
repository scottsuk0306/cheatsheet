# cheatsheet
Collection of commands that I use often

## Managing files

#### 1. See how large a file is.
```bash
ls -lh example.txt
```

#### 2. Sort files accroding to the file size
```bash
du -sh .[^.]* * | sort -h
```

## Git

#### 1. Reapply .gitignore
```bash
git rm -r --cached .
git add .
git commit -m "Reapply .gitignore"
```

#### 2. git clone but with a different directory name

```bash
git clone https://github.com/username/myproject.git myproject-clone
```


## Conda



## Huggingface
