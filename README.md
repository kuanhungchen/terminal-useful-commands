# Terminal Useful Commands #
### A list of terminal commands, git commands, and anything useful that I usually use. ###

- Login to server by using SSH  
  ```$ ssh <username>@<server_ip>```

- Login to server by using SSH on a specific port  
  ```$ ssh <username>@<server_ip> -p <port_ID>```

- (secure) copy files from server to local  
  ```$ scp -P <port_number> <username>@<server_ip>:<file_dir> <local_dir>```
  
- (secure) copy files from local to server  
  ```$ scp -P <port_number> <file_dir> <username>@<server_ip>:<server_dir>```

- Login to server by using sftp  
  ```$ sftp <username>@<server_ip>```
  
- Download from server by using sftp  
  ```$ get <file_name>```

- Monitor (NVIDIA) GPU status  
  ```$ nvidia-smi```  
  ```$ nvidia-smi -L```  
  ```$ nvidia-smi -q -i 0```  
  ```$ nvidia-smi -q -i 0 -x```  
  ```$ nvidia-smi -l 1```

- Clear the terminal screen  
  ```cmd + K```  
  ```ctrl + L```  

- Clear everything backwards to beginning of line  
  ```ctrl + U```

- View Trash directory in terminal  
  ```$ cd ~/.Trash```

- Delete all files in this directory  
  ```$ rm -f ./*```

- Make (hard) link (can overwrite but won't show linking location in ```ls -al```)  
  ```$ ln <source_file> <target_file>```

- Make symbolic link (can't overwrite but will show linking location in ```ls -al```)  
  ```$ ln -s <source_file> <target_file>```

- Download files  
  ```$ wget <url>```  
  ```$ wget -b <url>``` (download in the background)

- Create/Untar tar archive file  
  ```$ tar cvf <filename>.tar <dir_name>```  
  ```$ tar xvf <filename>.tar```

- Create/Uncompress gz archive file  
  ```$ gzip <filename>```  
  ```$ gunzip <filename>.gz```

- Create/Uncompress tar.gz archive file  
  ```$ tar cvzf <filename>.tar.gz <dir_name>```  
  ```$ tar xvf <filename>.tar.gz```

- Print last lines of file(s)  
  ```$ tail <filename>```  
  ```$ tail -n <N> <filename>``` (print last N lines of file)  
  ```$ tail -f <filename>``` (keep checking and printing new data)

- Find number of files under a folder  
  ```$ find . -type f | wc -l```

- Search keyword by regular expression  
  ```$ grep <keyword> <file1> <file2> ...```  
  ```$ ls <directory> | grep <keyword>```  
  ```$ grep -i <keyword> <file>``` (case not sensitive)  
  ```$ grep -n <keyword> <file>``` (indicate line number)  
  ```$ grep -v <keyword> <file>``` (inverse search)  
  ```$ grep -r <keyword> <file>``` (recursive search)  
  ```$ grep -A <N> <keyword> <file>``` (show extra N lines after keyword)  
  ```$ grep -B <N> <keyword> <file>``` (show extra N lines before keyword)  
  ```$ grep -C <N> <keyword> <file>``` (show extra N lines before and after keyword)  

- Edit file on remote by scp using (m)vim  
  ```$ (m)vim scp://username@hostname:port/path/to/file```

## git related ##

- Add branch  
  ```$ git branch <branch_name>```

- Switch branch  
  ```$ git checkout <branch_name>```

- Add a new remote  
  ```$ git remote add origin <URL>```

- Change URL of an existing remote repo  
  ```$ git set-url --add origin <URL>```

- Rename a repo from both server and local  
  1. rename the repo online  
  2. rename the filename of the repo locally  
  3. ```$ git remote (will see a remote name)```  
  4. ```$ git remote rm <remote_name>```  
  5. ```$ git remote add <new_remote_name> <new_url>```  
  6. ```$ git branch --set-upstream-to=<new_remote_name>/<branch_name>```

- Show the commit logs  
	```$ git log``` (add ```--oneline``` for one-line format)

- Show the changes between Working and Staging  
	```$ git diff```

- Show the changes between Staging and Repo  
	```$ git diff --cached```

- Show the changes between two commits  
	```$ git diff <commit1> <commit2>```

- Show the changes between Working and Repo  
	```$ git diff HEAD```

- For the remote tracking branches which are deleted, aka the stale branches  
	```$ git remote prune origin``` (remove those locally)  
	```$ git remote prune origin --dry-run``` (just list them)

## conda related ##

- Install package  
  ```$ conda install <package_name>```

- Remove package  
  ```$ conda remove <package_name>```

- Install specific verion of Python  
  ```$ conda install python=<python_version>```

- Create an environment with a specific version of Python  
  ```$ conda create -n <environment_name> python=<python_version>```

- Create an environment with a specific version of a package  
  ```$ conda create -n <environment_name> <package_name>=<package_version>```  
  ```$ conda install -n <environment_name> <package_name>=<package_version>```
  
- Create an environment with a specific package  
  ```$ conda create -n <environment_name> <package_name>```  
  ```$ conda install -n <environment_name> <package_name>``` (environment has already existed)
  
- Activate an environment 
  ```$ source activate <environment_name>```

- Deacticate an environment  
  ```$ source deactivate```

- Check pachages in environment  
  ```$ conda list```

- Check all environments  
  ```$ conda env list```

- Remove an environment  
  ```$ conda env remove -n <environment_name>```
