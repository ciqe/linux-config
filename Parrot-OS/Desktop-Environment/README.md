# Change Desktop Environment in Parrot OS

From version 5.0 LTS, ParrotOS is available with the default MATE Desktop Environment (DE) for all editions (Home, Security). However, other desktop environments like XFCE, KDE, etc... can be installed. Each DE has its peculiarity, but we recommend trying them out before deciding what to install (keep in mind that you can install multiple DEs on one OS). 

<br>

It may be useful to know that the user can install more DE on their Parrot, just type in a terminal:
```bash
sudo apt update && sudo apt install parrot-desktop-<desktop environment>
```
then restart your computer. In the login session you can change DE by clicking on the white dot ⚪️ (it's the "default session") and change DE. You can now use the newly installed DE with all the tools and configurations already present previously.

Example
```bash
sudo apt update && sudo apt install parrot-desktop-gnome
```

<br>

## Remove Desktop Environment:

```bash
sudo apt remove parrot-desktop-<desktop environment>
```

## Uninstall parrot-mate and its dependencies

```bash
sudo apt-get remove --auto-remove parrot-desktop-mate
```

This will remove the parrot-mate package and any other dependant packages which are no longer needed.

<br>

## Purging your config/data too

If you also want to delete your local/config files for parrot-mate then this will work.

### Caution! Purged config/data can not be restored by reinstalling the package.

```bash
sudo apt-get purge --auto-remove parrot-desktop-mate
```



<hr>

### Source:
* https://parrotsec.org/docs/desktop-enviroments.html
* https://installlion.com/parrot/jollyroger/main/p/parrot-mate/uninstall/index.html
