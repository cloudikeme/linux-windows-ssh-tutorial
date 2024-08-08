### Install OpenSSH-Server in WSL

First, install OpenSSH server inside your Linux Distro:

sudo apt install openssh-server  


### On client machine

for linux
ssh-keygen -t rsa -f ~/.ssh/id_rsa
cat ~/.ssh/id_rsa.pub
copy the pub key 

### On server machine (windows that contains wsl)

save the copied key in documents folder as pub_key
right click on file and copy as path ( note this path address, you would need this later)
open powershell as admin
Run the command below. The output shows `True` when you're a member of the built-in Administrators group.

```bash
(New-Object Security.Principal.WindowsPrincipal([Security.Principal.WindowsIdentity]::GetCurrent())).IsInRole([Security.Principal.WindowsBuiltInRole]::Administrator)
```


for an admin user 
cp "C:\Users\Victo\Documents\pub_key.txt" "$env:programdata\ssh\administrators_authorized_keys"


for windows
ssh-keygen.exe -t rsa -f $env:USERPROFILE\.ssh\id_rsa


 
