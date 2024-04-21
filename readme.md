# Arch User Repository

[tomcat0x42's](https://aur.archlinux.org/account/tomcat0x42) personal pacman repo.

Mainly includes a personal config of the [LLVM](https://llvm.org/) project packages and the AUR packages that I maintain.

## Import my PGP key

Import my GPG key from a keyserver:

```bash
sudo pacman-key --recv-keys D53B2A48C41BD647042FAD1059146EDE9B2F2872 
```

Or alternatively directly from the keyfile:

```bash
wget tomcat0x42.me/aur/assets/tomcat0x42.gpg && sudo pacman-key --add tomcat0x42.gpg
```

And verify/sign the key:

```bash
sudo pacman-key --finger D53B2A48C41BD647042FAD1059146EDE9B2F2872 && sudo pacman-key --lsign-key D53B2A48C41BD647042FAD1059146EDE9B2F2872
```


## Add the repo to pacman

Add the following to `/etc/pacman.conf`:
	
```
[tomcat0x42]
Server = https://tomcat0x42.me/aur/
```
