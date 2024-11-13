# multipleSSH
Scripts to aid ssh copy/download/exec on multiple servers multi-threaded

You must have the same username and password on all machines.
To set username and password
```
export SSH_USERNAME=Redacted
export SSH_PASSWORD=Redacted
```

> you can also use {ip} in the `command`
```
usage: sshcopy [-h] [--download] file local_path remote_path

Copy files to/from multiple machines using SCP.

positional arguments:
  file         Path to the file containing IP addresses
  local_path   Path to the local file or directory
  remote_path  Path on the remote machine

options:
  -h, --help   show this help message and exit
  --download   Download files from remote to local (default is upload)
```

```
usage: sshexec [-h] [-v] file command

Execute SSH commands on multiple machines.

positional arguments:
  file           Path to the file containing IP addresses
  command        Command to execute on each machine. Use {ip} to include the IP in the command.

options:
  -h, --help     show this help message and exit
  -v, --verbose  Enable verbose output
```
 
> This also works with sudo, but to work sudo needs to be at the start of command. ex: `sudo rm example`
