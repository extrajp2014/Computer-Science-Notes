# Set up Multiple ssh-keys for different GitHub accounts on one computer

## Generate ssh keys for account1 and account2
```bash
ssh-keygen -t rsa -b 4096
```
- Example rsa key names
> account1_rsa
> account2_rsa

## Modify ssh config file to route ssh keys
vim ~/.ssh/config
```
# Account1 GitHub account
Host github.com
 HostName github.com
 User git
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/account1_rsa

# Account2 GitHub account
Host github.com-account2
 HostName github.com
 User git
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/account2_rsa
```

## Git clone project 
- Using account1
```bash
git@github.com:[github_acount_name]/[my project].git
# eg. git@github.com:extrajp2014/Computer-Science-Notes.git
```

- Using account2
```bash
git@github.com-account2:[github_acount_name]/[my project].git
# eg. git@github.com-account2:extrajp2014/Computer-Science-Notes.git
```