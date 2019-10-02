This personal repository contains build code for Visual Studio Code based from Arch Linux community repository with applied patch from Coler706 at https://github.com/coler706/vscode (without monokai theme fixes, sorry) and a few fixes (attempts at least) from me.

In overall, this enabled VS Code to have tranparent window which looks sick in combination with KDE Plasma, for example.

======

To install clone this repository and run "makepkg -i" or either download latest release archive (x86_64 only) and use "pacman -U code-[version]-[arch].pkg.tar.xz".

======

(i) For KDE be sure to either manually enable blur for code-oss windows or install plugin Force Blur https://store.kde.org/p/1294604 and in its settings add "code-oss" window class.

(!) Sometimes it would fail to be transparent from cold start, just start one more window and reopen first (failed) one.

(i) It will probably need your fixes. This is easily done using settings.json file where you can add something like this:

---
    "workbench.colorCustomizations": {
        "editor.background": "#0f0f0f60",
        "menu.background": "#222222",
        "sideBar.background": "#1d1d1de0",
        "titleBar.activeBackground": "#111111e0",
        "activityBar.background": "#111111e0",
        "editorGroupHeader.tabsBackground": "#1d1d1de0",
        "statusBar.background": "#005c99e0",
        "terminal.background": "#0f0f0f60",
        "terminal.ansiBlack": "#0f0f0f60",
        "panel.background": "#0f0f0fd9",
    },
---

=======

THIS IS NOT COMPLETE PACKAGE AND NOT READY FOR PUBLISHING IN AUR, but it's working and you'll be able to install it, replacing original community's "code". I (and Coler706 probably) will be happy if someone will be able to fork this repository, fix PKGBUILD, redo "transparency" patch and create normal AUR package.