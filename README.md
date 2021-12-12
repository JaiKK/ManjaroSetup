# ManjaroSetup
Essential software and configuration for Manjaro


# Locate (for faster search)

sudo pacman -S mlocate
or
sudo pacman -S plocate

sudo updatedb

### ***Links***
https://wiki.archlinux.org/title/locate
https://archlinux.org/packages/core/x86_64/mlocate/
https://archlinux.org/packages/community/x86_64/plocate/

---

-=-=-=-=--=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-

---

# Github SSH setup

ssh-keygen -t ed25519 -C "jaikuraria@gmail.com"

eval "$(ssh-agent -s)"

ssh-add ~/.ssh/id_ed25519

cat ~/.ssh/id_ed25519.pub

ssh -T git@github.com


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