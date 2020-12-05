# Collection of hints and tipps to get the environment running

## Ubuntu 20.04 LTS on Intel system

### ssh connection after reboot take several minutes

option 1:  
Edit /etc/ssh/sshd_config and set GSSAPIAuthentication=no

option 2:  
Edit ~/.ssh/config and add  
```bash
Host *
  GSSAPIAuthentication no
```

## Git

### Using dedicated private key for github

Copy private key into ~/.ssh/

Edit ~/.ssh/config and add

```bash
Host github.com
  User git
  Hostname github.com
  IdentityFile ~/.ssh/<your_private_key_file>
```

Don't forget to set the required permissions

```bash
chmod 600 ~/.ssh/<your_private_key_file>
```


