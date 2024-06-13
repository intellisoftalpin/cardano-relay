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
PORT=3001
METRICS_PORT=12798
```

CNODE_IPC - path to socket file   
CNODE_DATA - path to bloackchain data   
CNODE_CONF_BASE - path to configuration folder   
PORT - Cardano node port 
METRICS_PORT - default port for prometheus metrics

### Allow the ports in the host firewall

```bash
sudo ufw allow 3001
sudo ufw allow 12798
```

### Run the server

Use the following commands to work with cardano service

#### Start the service

```bash
cnode start 
```

#### Stop the service

```bash
cnode status 
```

#### Status of the service

```bash
cnode status 
```

#### Synchronization status of the service

```bash
cnode syncstatus 
```

#### Status of the service

```bash
cnode status 
```


