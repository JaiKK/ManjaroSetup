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
ssh-keygen -t ed25519 -C "jaikuraria@gmail.com"

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

ftp

---

-=-=-=-=--=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

---

apparmor

---

-=-=-=-=--=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

---