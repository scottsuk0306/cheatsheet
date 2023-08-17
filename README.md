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

#### 3. See usage of a whole file system

```bash
df -h
```

#### 4. Determine the device of the directory

```bash
df -h directory_name
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

#### 1. Install conda
```bash
wget https://repo.continuum.io/archive/Anaconda3-2023.03-Linux-x86_64.sh
bash Anaconda3-2023.03-Linux-x86_64.sh
```

## Huggingface

## Tmux

#### 1. Install tmux
```bash
sudo apt-get install tmux
```
