ubuntu-14.04-seedbox
====================
### Update & Upgrade Server
```
sudo apt-get update && sudo apt-get upgrade -y
```

### Install Prerequisites
```
sudo apt-get install python-software-properties && add-apt-repository ppa:transmissionbt -y
```
### Install Transmission Daemon 
```
sudo apt-get update
``` 
```
sudo apt-get install transmission-daemon
```
### Update Transmission Password
```
sudo nano /etc/transmission-daemon/settings.json
```
#### Find And Replace rpc-password and rpc-whitelist-enabled as shown. 
```
"rpc-password": "YourNewPassword",
```
###### Replace the above with an appropriate password. 
```
"rpc-whitelist-enabled": false,
```
### Save and Exit
```
"ctrl+x" and "y"
```

### Reload Transmission 
```
sudo /etc/init.d/transmission-daemon reload
```

That's all. To use your new seedbox go to your web browser and type your server's ip with port 9091. Example http://111.222.33.444:9091/.
A dialog box should pop up, enter **transmission** as the username and the password you created. 
