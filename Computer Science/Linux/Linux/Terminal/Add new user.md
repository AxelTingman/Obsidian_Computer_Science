#Operating_System/Linux 

#### Add new user
``useradd`` *username*

#### Set new password
``passwd`` *username*!


#### Add sudo permissions to user
1. ``sudo visudo``
2. If the username is ``axel`` add the user by adding the line ``axel     ALL=(ALL:ALL) ALL`` to the document.

[[Screenshot from 2022-03-13 13-00-30.png]]