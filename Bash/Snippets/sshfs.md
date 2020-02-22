mount the remote linux folder on mac

```bash
sshfs -o IdentityFile=~/.ssh/id_rsa myuser@myserver:/my/remote/folder /my/local/folder
```