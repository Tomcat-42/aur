![arch_logo](https://github.com/Tomcat-42/aur/assets/44649669/bc6c8427-2061-4c43-8a23-95c74946a335)

> [Tomcat0x42's](https://aur.archlinux.org/account/tomcat0x42) personal pacman repo.
> 
> Mainly includes a personal config of the [LLVM](https://llvm.org/) project packages and the AUR packages that I maintain.

<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->

- [Import my PGP key](#import-my-pgp-key)
- [Add the repo to pacman](#add-the-repo-to-pacman)
- [Packages](#packages)

<!-- TOC end -->

<!-- TOC --><a name="import-my-pgp-key"></a>
## Import my PGP key

Import my GPG key from a keyserver:

```bash
sudo pacman-key --recv-keys D53B2A48C41BD647042FAD1059146EDE9B2F2872 
```

Or alternatively directly from the keyfile:

```bash
wget tomcat0x42.me/aur/tomcat0x42.gpg && sudo pacman-key --add tomcat0x42.gpg
```

And verify/sign the key:

```bash
sudo pacman-key --finger D53B2A48C41BD647042FAD1059146EDE9B2F2872 && sudo pacman-key --lsign-key D53B2A48C41BD647042FAD1059146EDE9B2F2872
```

<!-- TOC --><a name="add-the-repo-to-pacman"></a>
## Add the repo to pacman

Add the following to `/etc/pacman.conf`:
	
```bash
[tomcat0x42]
Server = https://tomcat0x42.me/aur/$arch
```

And finally, sync pacman database:

```bash
sudo pacman -Sy
```

<!-- TOC --><a name="packages"></a>
## Packages

| **_name_**                | **_description_**                                                                                                                                     | **_upstream url_**                                    |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| cmake-git                 | CMake is a cross-platform, open-source build system generator.                                                                                        | https://gitlab.kitware.com/cmake/cmake                |
| llvm-git                  | My build of the LLVM project. Includes experimental clangd modules support  (https://github.com/llvm/llvm-project/pull/66462#issuecomment-2047747705) | https://llvm.org/                                     |
| llvm-runtimes-git         | My build of the LLVM runtimes (libc++, libc++abi and libunwind).  Includes libc++ modules installation.                                               | https://llvm.org/                                     |
| mesa-git                  | Open source implementations of OpenGL, OpenGL ES, Vulkan, OpenCL, and more. Built against this repo LLVM.                                             | https://www.mesa3d.org                                |
| sandbar-git               | dwm-like bar for the river wayland compositor                                                                                                         | https://github.com/kolunmi/sandbar                    |
| spirv-llvm-translator-git | A tool and a library for bi-directional translation between SPIR-V and LLVM IR. Build against this repo LLVM.                                         | https://github.com/KhronosGroup/SPIRV-LLVM-Translator |
