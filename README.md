# Terminal Useful Commands
### A list of terminal commands, git commands, and anything useful that I usually use.

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

## git related

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
