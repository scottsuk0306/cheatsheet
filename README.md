# cheatsheet
Collection of commands that I use often

## Managing files

#### 1. See how large a file is.
```bash
ls -lh example.txt
```

#### 2. Sort files accroding to the file size

- In the current directory
```bash
du -sh .[^.]* * | sort -h
```

- Recursively search in the current directory, for files larger than 100MB
```bash
find . -type f -size +100M -exec du -h {} + | sort -h
```

#### 3. Sort Users according the the used up space
```bash
sudo du -sh /home/* | sort -h
```

#### 4. See usage of a whole file system

```bash
df -h
```

#### 5. Determine the device of the directory

```bash
df -h directory_name
```

#### 6. Check how much space the current directory takes up
```bash
du -sh .
```

## Docker

#### 1. Run docker container with mounted directory and gpus attached, in detach mode
```bash
docker run --gpus all -v /mnt/sda/{your_directory}:/home/{your_username} -d --name {container_name} {image_name}
```

#### 2. Run docker container with gpus attached, in detach mode
```bash
docker run --gpus all -d --name {container_name} {image_name}
```


#### 3. Interact with a running container
```bash
docker exec -it {container_name} /bin/bash
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

#### 2. Create a new environment
```bash
conda create -n env_name python=3.9
```

#### 3. Manually configure the installation path for conda environments and packages 
```bash
conda config --prepend pkgs_dirs [PATH]
conda config --prepend envs_dirs [PATH]
```

## Huggingface

## Tmux

#### 1. Install tmux
```bash
sudo apt-get install tmux
```

## Poetry

#### 1. Remove poetry env
```bash
poetry env remove $(which python)
```
