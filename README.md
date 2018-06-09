# Wino Masternodes Setup for Windows + Linux

## Following these instructions, you will be able to install and configure masternode on your VPS server. To ensure funds security, the "hot" wallet will be managed by the "cold" one. 

## Ubuntu 16.04 64bit server should always be connected to the Internet and power supply. Make sure that parameters of your machine meet the minimum system requirements: Minimum 10GB free on SSD, 1GB of RAM, VPS with a unique IP address.

## First, set up the "cold" wallet :

### Make sure that you have the latest version of the wino-qt wallet installed and synchronize it;
### For the correct setting up, you need to have at least 5000 WINO on the account. If there are not enough funds, the balance must be replenished;
### To ensure security, you need to backup the file wallet.dat. Copy it to another computer. Before that, remember to enable encryption.

## If the computer meets the requirements, you have to perform the following actions in the server console (opens via the Tools menu) :

### Use masternode genkey command to get your private key. Do not forget to copy the private key to a safe place;
### Use the getaccountaddress command MASTERNODE to get the masternode address. The received address (MASTERNODE_ADDRESS) is required for token transfer. If necessary, change MASTERNODE to MASTERNODE_ALIAS_NAME;
### In the "Send" tab, send money to your masternode address;
### Transaction outputs can be viewed via masternode outputs command;
### Using notepad, edit the masternode configuration file, which is called masternode.conf. The data should look like this: MASTERNODE_ALIAS_NAME VPS_IP:27781 MASTERNODE_PRIVATKEY TX_ID TX_INDEX;
### After writing down the masternode data in the data file, save masternode.conf.

## Using an SSH client, you have to log in to VDS with root rights and start the script by the following command:
### wget https://raw.githubusercontent.com/WinoDev/MN-guide/master/auto-install.sh
### bash auto-install.sh

## If necessary, enter MASTERNODE_PRIVATKEY. Now you can launch the masterpiece in the "Masternode" menu in the "cold" wallet. You can view status of the installed and configured masternode via wino-cli masternode status command.

