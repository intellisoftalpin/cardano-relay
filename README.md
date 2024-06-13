
# Cardano Relay Setup
A Docker Compose file to quickly set up a Cardano relay.

## Installation Guide

### Setting Path to cnode Script

Set the PATH to the `scripts/` folder, so the `cnode` script is available anywhere. 

In the `cnode` file, change the `env` variable to the compose file, if the path is different on your machine.

### Creating Environment Variables for Cardano Files on Your Host

Create a `.env` file in the same folder where the Docker Compose file is located with the following variables:

```bash
CNODE_IPC="/your/path/cardano-node/ipc"
CNODE_DATA="/your/path/cardano-node/data"
CNODE_CONF_BASE="/your/path/cardano-node/config"
PORT=3001
METRICS_PORT=12798
```

- `CNODE_IPC`: Path to the socket file
- `CNODE_DATA`: Path to the blockchain data
- `CNODE_CONF_BASE`: Path to the configuration folder
- `PORT`: Cardano node port
- `METRICS_PORT`: Default port for Prometheus metrics

### Allowing the Ports in the Host Firewall

```bash
sudo ufw allow 3001
sudo ufw allow 12798
```

### Running the Server

Use the following commands to work with the Cardano service:

#### Start the Service

```bash
cnode start 
```

#### Stop the Service

```bash
cnode stop 
```

#### Service Status

```bash
cnode status 
```

#### Synchronization Status of the Service

```bash
cnode syncstatus 
```

#### Cardano Node Version Information

```bash
cnode version 
```

#### Cardano Node Size on the Host

```bash
cnode size 
```
