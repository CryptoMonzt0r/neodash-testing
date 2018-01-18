Multi masternode config
=======================

The multi masternode config allows to control multiple masternodes from a single wallet. The wallet needs to have a valid collaral output of 1000 coins for each masternode. To use this, place a file named `masternode.conf` in the data directory of your install:
 * Windows: %APPDATA%\Neodash\
 * Mac OS: ~/Library/Application Support/Neodash/
 * Unix/Linux: ~/.neodash/

`masternode.conf` format is a space seperated text file. Each line consisting of an alias, IP address followed by port, masternode private key, collateral output transaction id and collateral output index.

Example:
```
mn1 127.0.0.2:17135 93HaYBVUCYjEMeeH1Y4sBGLALQZE1Yc1K64xiqgX37tGBDQL8Xg 2bcd3c84c84f87eaa86e4e56834c92927a07f9e18718810b92e0d0324456a67c 0
mn2 127.0.0.3:17135 93WaAb3htPJEV8E9aQcN23Jt97bPex7YvWfgMDTUdWJvzmrMqey aa9f1034d973377a5e733272c3d0eced1de22555ad45d6b24abadff8087948d4 0
mn3 127.0.0.4:17135 92Da1aYg6sbenP6uwskJgEY2XWB5LwJ7bXRqc3UPeShtHWJDjDv db478e78e3aefaa8c12d12ddd0aeace48c3b451a8b41c570d0ee375e2a02dfd9 1
```

In the example above:
* the collateral for `mn1` is output `0` of transaction http://test.explorer.neodash.fr/tx/2bcd3c84c84f87eaa86e4e56834c92927a07f9e18718810b92e0d0324456a67c and it has amount of 1000 NDASH


The following new RPC commands are supported:
* list-conf: shows the parsed masternode.conf
* start-alias \<alias\>
* start-missing
* start-disabled
* start-many
* outputs: list available collateral output transaction ids and corresponding collateral output indexes

When using remote masternode setup, you **must** remove `masternode=1` from local `neodash.conf` file if you had it there in previous versions. This option should be used only to start local Hot masternode now.
