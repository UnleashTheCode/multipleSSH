# multipleSSH
Scripts to aid ssh copy/download/exec on multiple servers multi-threaded


usage: sshcopy [-h] [--download] file local_path remote_path

Copy files to/from multiple machines using SCP.

positional arguments:
  file         Path to the file containing IP addresses
  local_path   Path to the local file or directory
  remote_path  Path on the remote machine

options:
  -h, --help   show this help message and exit
  --download   Download files from remote to local (default is upload)


usage: sshexec [-h] file command
> for this you can alos use {ip} in the `command`
Execute SSH commands on multiple machines.

positional arguments:
  file        Path to the file containing IP addresses
  command     Command to execute on each machine. Use {ip} to include the IP in the command.

options:
  -h, --help  show this help message and exit
