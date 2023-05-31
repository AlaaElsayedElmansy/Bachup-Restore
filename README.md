# Secure-Backup-Restore

## About The Scripts
Here two bash scripts we can use them if we need to make secure backup to our system OR we need to restore backup to our system.


## 🛠 Tools :
| Tool | Purpose |
| ------ | ------ |
| [ Tar ](https://www.tutorialspoint.com/linux-tar-command) | Tar is used to create and extract archive files. |
| [gnupg ](https://www.poftut.com/install-use-gpg-encrytion-linux-order-encrypt-decrypt-files-folder/) |  It provides encryption, decryption, digital signatures, and signing.. |
| [ Scp ](https://linuxhint.com/linux_scp_command/) | It is used to securely copy files between two servers. |




## Requirements
  Make sure all Tools are installed.


## Steps:
 - Clone The Project
  ```bash
     git clone https://github.com/AlaaElsayedElmansy/Bachup-Restore
  ``` 
 - Excute scripts
 ```bash
    chmod +x backup.sh
    chmod +x restore.sh
``` 

## Run backup.sh
- Before tring run the script
```bash
you need to make sure that you have 4 paramters:
1)The directory that contains the backup 
2)the directory which should store eventually the backup 
3)The Key 
4)Number of Days 
```
- Run
```bash
    . backup.sh /path to the source /path to backup to "key" "days"
``` 
## Run restore.sh
- Before Run
```bash
you need to make sure that you have 3 paramters:
1)The directory that contains the backup
2)the directory to restore to
3)The Key
```
 - Run
 ```bash
    . restore.sh /source path /destintion path "the same key of backup"
 ``` 
# Copying to remote server
- Preparing source server and destination server
You can follow this steps in the link below
```bash
https://blog.microideation.com/2016/05/26/secure-copy-files-scp-between-two-ec2-instances-in-aws/
```
- OR you can ssh the other server
- uncomment this line in backup_restore_lib.sh and adjust it.
```bash
scp -i ~/main.pem $dest/$now.tar.gz.gpg @username:/home/ubuntu/data
```
- Run bach.sh again !!



