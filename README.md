# Notes Deployment


## Configure SECRET VARIABLE
```bash
HOST --> IP public server
KEY --> ssh or file .pem
PORT --> 22
USERNAME --> ubuntu 

# for DB
DB_HOST --> rds: endpoint, gcp: ip database server
DB_NAME --> database name
DB_USERNAME
DB_PASSWORD
DB_PORT --> 3306

```


## When Error ssh handshake failed
```bash
# https://github.com/appleboy/ssh-action/issues/80#issuecomment-1032124504

echo "PubkeyAcceptedKeyTypes=+ssh-rsa" >> /etc/ssh/sshd_config

# dont forget to restart server
# and make sure PubkeyAcceptedKeyTypes=+ssh-rsa was added
# https://bbs.archlinux.org/viewtopic.php?id=270005
cat /etc/ssh/sshd_config
```