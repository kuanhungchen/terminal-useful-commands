# terminal_useful_command

- Login to server by using SSH  
  - ssh <username>@<server_ip>

- Login to server by using SSH on a specific port  
  - ssh <username>@<server_ip> -p <port_ID>

- copy from server to local  
  - scp -P <port_number> <username>@<server_ip>:<file_dir> <local_dir>

- Monitor (NVIDIA) GPU status  
  - nvidia-smi  
  - nvidia-smi -L  
  - nvidia-smi -q -i 0  
  - nvidia-smi -q -i 0 -x  
  - nvidia-smi -l 1

- Clear the terminal screen
  - cmd + K
  - ctrl + L
