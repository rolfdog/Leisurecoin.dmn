# Leisurecoin.dmn

wget https://github.com/rolfdog/Leisurecoin.dmn/blob/master/dmn.sh

wget https://raw.githubusercontent.com/LeisureCoinProject/LeisureCoin-Core-Masternode/master/leisure_mn_simple_setup.sh

wget https://github.com/rolfdog/Leisurecoin.dmn/blob/master/Dumpmn.sh

#Set-Up $5 VPS with at least 2GB RAM.

#Install first MN as usual manually. Set-up desktop wallet same (private key, Tx, Output Code). 

#Make sure dupmn_install.sh and LeisureCoin.dmn are on your VPS (we may want to host them so we can use WGET)

#Make following commands on VPS 

apt-get install lsof

apt-get install curl

bash dupmn_install.sh

dupmn profadd LeisureCoin.dmn LeisureCoin

#Wait until your first MN fully syncs (Important)

#You will have your first MN and the following commands will add a copy of it instantly.

#You can add up to 7 MNs

#Initial MN created above will just be LeisureCoin-cli, then second will be LeisureCoin-cli-1, third will be LeisureCoin-cli-2, 

etc.

#For second MN

dupmn install LeisureCoin 

dupmn bootstrap LeisureCoin 1

#Copy Private Key and IP Address:Port that will be presented after install. This will go in your desktop wallet set-up.

LeisureCoin-cli-1 getinfo

LeisureCoin-cli-1 masternode status

#For third MN

dupmn install LeisureCoin 

dupmn bootstrap LeisureCoin 2

#Copy Private Key and IP Address:Port that will be presented after install. This will go in your desktop wallet set-up.

LeisureCoin-cli-2 getinfo

LeisureCoin-cli-2 masternode status

#Same thing for additional MNs up to a max of 7 total on VPS

#Once all VPS MNs are installed make sure to update Private Keys and IP Address:Port on desktop wallet conf files and restart 

desktop wallet and start MNs on desktop.

Extra Commands:

LeisureCoin-cli-all masternode status

You can find more commands and instructions in the following link:

https://github.com/neo3587/dupmn/blob/master/README.md
