#Operating_System/Linux/Package_Manager/APT 

## [[APT|APT]]
In apt there are two ways to uninstall a package:

>sudo apt remove [package name]

or 

>sudo apt purge [package name]

### What’s the difference between ‘**_remove_**‘ and ‘**_purge_**‘ ?

So the begging question here is ‘**_remove_**‘ and ‘**_purge_**‘ and when to use what ?

The primary difference being ‘**_remove_**‘ and ‘**_purge_**‘ is that ‘**_remove_**‘ only gets rid of the package leaving any configuration files untouched. Whereas ‘**_purge_**‘ not only removes the package but also removes all configuration files OUTSIDE THE HOME DIRECTORY.

