# newkeydebianrepo
add new key from ubuntu com to apt-get system

#!/bin/bash
apt-key adv --recv-keys --keyserver keyserver.ubuntu.com `sudo apt-get update 2>&1 | grep -o '[0-9A-Z]\{16\}$' | xargs`


if error 
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory

just 
sudo apt-get install dirmngr
