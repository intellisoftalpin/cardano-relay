# Cardano Relay setup
Docker compose file to quickly setup cardano relay 

## Installation guide

### Setting path to cnode script

Set the PATH to the scripts/ folder, so the cnode script available anywhere

in cnode file change the env variable to the compose file, if the path is different on your machine

### Create env variables to location of cardano files on your host

Create in the same folder where docker-compose file is located the .env file with the following variables

```bash
CNODE_IPC="/your/path/cardano-node/ipc"
CNODE_DATA="/your/path/cardano-node/data"
CNODE_CONF_BASE="/your/path/cardano-node/config"
```

CNODE_IPC - path to socket file   
CNODE_DATA - path to bloackchain data   
CNODE_CONF_BASE - path to configuration folder   

### Correct docker-compose file if necessary

If you need to change the 
