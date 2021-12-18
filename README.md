# ManjaroSetup
Essential software and configuration for Manjaro


# Locate (for faster search)

Install locate
```shell
sudo pacman -S mlocate
```
or
```shell
sudo pacman -S plocate
```
Update search DB
```shell
sudo updatedb
```
### ***Links***
https://wiki.archlinux.org/title/locate

https://archlinux.org/packages/core/x86_64/mlocate/

https://archlinux.org/packages/community/x86_64/plocate/

---

-=-=-=-=--=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

---

# Github SSH setup

Create and add private key to ssh agent
```shell
ssh-keygen -t ed25519 -C "email@gmail.com"

eval "$(ssh-agent -s)"

ssh-add ~/.ssh/id_ed25519
```

Copy and paste public key to github.
```shell
cat ~/.ssh/id_ed25519.pub
```
Check the connectivity
```shell
ssh -T git@github.com
```

### ***note***:
to use SSH you must use SSH link of project and not HTTPS.

### ***Links***
https://wiki.archlinux.org/title/SSH_keys

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/about-ssh

https://docs.github.com/en/authentication/troubleshooting-ssh


---

-=-=-=-=--=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

---

flatpak search vscode
flatpak install com.visualstudio.code
flatpak run com.visualstudio.code


---

-=-=-=-=--=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

---

snap find vscode
snap install --classic vscode
snap run code

---

-=-=-=-=--=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

---

samba

---

-=-=-=-=--=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

---

# FTP

```shell
docker run -d -p 21:21 -v /my/data/directory:/home/vsftpd --name vsftpd fauria/vsftpd
```

```shell
mkdir /home/test/ftpdata
chmod 777 /home/test/ftpdata
```

```shell
docker run -d -p 21:21 -v /home/test/ftpdata:/home/vsftpd --name vsftpd fauria/vsftpd
```

```shell
docker logs vsftpd
```

```shell
sudo docker run -d -v /home/test/ftpdata:/home/vsftpd \
-p 20:20 -p 21:21 -p 21100-21110:21100-21110 \
-e FTP_USER=myuser -e FTP_PASS=mypass \
-e PASV_ADDRESS=127.0.0.1 -e PASV_MIN_PORT=21100 -e PASV_MAX_PORT=21110 \
--name vsftpd --restart=always fauria/vsftpd
```

```shell
sudo docker run -d -v /home/test/ftpdata:/home/vsftpd \
-p 20:20 -p 21:21 -p 21100-21110:21100-21110 \
-e FTP_USER=myuser -e FTP_PASS=mypass \
-e PASV_ADDRESS=192.168.1.103 -e PASV_MIN_PORT=21100 -e PASV_MAX_PORT=21110 \
--name vsftpd --restart=always fauria/vsftpd
```

### ***note***:
1. WinScp and Filezilla gets an error *"500 OOPS: priv_sock_get_cmd"* and connection gets drop. Same happens if you connect and run "*dir*" or "*ls*" command. To resolve this issue add below line in the config.  
**seccomp_sandbox=no**  


2. PASV_ADDRESS ip address should be same as ftp server's public ip else passive connections will not work.

### ***Links***
https://hub.docker.com/r/fauria/vsftpd  
https://github.com/stilliard/docker-pure-ftpd  
https://technologytales.com/2013/09/21/turning-off-seccomp-sandbox-in-vsftpd/  

---

-=-=-=-=--=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

---

apparmor

---

-=-=-=-=--=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

---

tmux

---

-=-=-=-=--=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

---