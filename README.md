## ZeroTier for Github Actions

Allows for you to join ZeroTier in a Github Action.
Uses the identity of an existing ZeroTier node to join the network.

To get the config below, you should setup a ZeroTier Node with the correct access (in case you are using the network rules). Then, extract the contents indicated for each config, and delete the contents of `/var/lib/zerotier-one/` to ensure there are no identity conflicts.

## Config
### `zerotier-network`
The ZeroTier Network ID that you want to join

### `zerotier-node-authtoken`
The contents of `/var/lib/zerotier-one/authtoken.secret`

### `zerotier-node-publicidentity`
The contents of `/var/lib/zerotier-one/identity.public`

### `zerotier-node-secretidentity`
The contents of `/var/lib/zerotier-one/identity.secret`

### `zerotier-startup-maxconnect`
The maximum amount of time the action should wait for the ZeroTier Node to connect to ZeroTier Central.
Default is 300s

### `zerotier-startup-maxjoin`
The maximum amount of time the action should wait for the ZeroTier Node to finish connecting to the ZeroTier Network
Default is 300s