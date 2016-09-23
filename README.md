# Corebird Flatpak

This is a `flatpak-builder` definition file to build both corebird master and current stable branches.

Due to corebird opening a browser whenever a link is clicked, as well as when setting up an account, you need to have `xdg-desktop-portal` installed.

First, create the repository:

```shell
flatpak --user remote-add -from=baedert.flatpakrepo
```
or:
```shell
wget https://baedert.org/repo/baedert-repo.gpg
flatpak --user remote-add baedert-repo --gpg-import=baedert-repo.gpg https://baedert.org/repo
```

Now you can install corebird from the repo:
```shell
# for the current stable version
flatpak --user install baedert-repo org.baedert.corebird stable

# for the lastest unstable version
flatpak --user install baedert-repo org.baedert.corebird master
```

... and run it:
```shell
flatpak run org.baedert.corebird
```
