## These are my LOCAL (my machines) config for git public key

 johaGL

type :
```
git config --global user.name "johaGL"
git config --global user.email "johanna.galvis@ibgc.cnrs.fr"
git config --global core.editor "vim"
ssh-keygen -t rsa -b 4096 -C "johanna.galvis@ibgc.cnrs.fr"
```
 terminal messages, here I put also answers I give after `:` :
 ```
# Generating public/private rsa key pair.
# Enter file in which to save the key (/home/johanna/.ssh/id_rsa): /home/johanna/.ssh/id_rsa202202
# Enter passphrase (empty for no passphrase):  jo
# Enter same passphrase again:   jo
# Your identification has been saved in /home/johanna/.ssh/id_rsa202202
# Your public key has been saved in /home/johanna/.ssh/id_rsa202202.pub
```
type:
```
cat /home/johanna/.ssh/id_rsa202202.pub 
```
and copy the content into settings. 

 **as file has unusual name, do `ssh-add`** as follows:
 
```ssh-add ~./ssh.id_rsa202202``` 

terminal messages:
```
# @@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
# @         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
```

 **solved**: https://www.howtogeek.com/168119/fixing-warning-unprotected-private-key-file-on-linux/ 
 (thanks LOWELL HEDDINGS)
```
sudo chmod 600 ~/.ssh/id_rsa202202
sudo chmod 600 ~/.ssh/id_rsa202202.pub
ssh-add ~/.ssh/id_rsa202202
```
terminal messages (answer jo)
```
Enter passphrase for /home/johanna/.ssh/id_rsa202202: jo
```
finally I can git pull and everything :D
