# Terminal Useful Commands #
### A list of terminal commands, git commands, and anything useful that I usually use. ###

- Login to server by using SSH  
  ```$ ssh <username>@<server_ip>```

- Login to server by using SSH on a specific port  
  ```$ ssh <username>@<server_ip> -p <port_ID>```

- copy from server to local  
  ```$ scp -P <port_number> <username>@<server_ip>:<file_dir> <local_dir>```

- Monitor (NVIDIA) GPU status  
  ```$ nvidia-smi```  
  ```$ nvidia-smi -L```  
  ```$ nvidia-smi -q -i 0```  
  ```$ nvidia-smi -q -i 0 -x```  
  ```$ nvidia-smi -l 1```

- Clear the terminal screen  
  ```cmd + K```  
  ```ctrl + L```  

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
