# *PRIVATE* Unreal Tournament 2004 Dedicated LAN Server -  Credits to: Laclede's LAN

This repo is forked off of the [Laclede's LAN UT2004-Freeplay Server](https://github.com/LacledesLAN/gamesvr-ut2004-freeplay). This is a private Docker image designed so that I can host a private LAN server with family members and friends.

It should be compatible on UGreen OS, also known as UGOS, which is essentially rebadged Debian.

== THIS MAY NOT BE UPDATED FREQUENTLY, IF AT ALL ==

### To run the server:

```shell
docker run -it --rm --net=host tdns07/ut2004-lan-svr:[VER_NO] ./ucc-bin server [MAP_NAME]?game=[GAME_MODE]?NumBots=8?Difficuty=3?MinPlayers=8?mutator=[MUTATOR_CLASS_NAME] -ini=UT2004-custom.ini -nohomedir -lanplay
```
### The commands / info, explained:

`[VER_NO]` = The version number of the file. It will likely be "master" / "latest" on here, but on [DockerHub](hub.docker.com/repository/docker/tdns07/ut2004-lan-server/), it should have version numbers

`[MAP_NAME]` = The map name, in full *with the gamemode prefix included*. An example is something like `GAMEMODE-MAPNAME`

`[GAME_MODE]` = The game mode, in full. 

`[MUTATOR_CLASS_NAME]` = The mutator / mod name, as it appears in it's `.ucl` file.

`-lanplay` = Makes the server exist solely on LAN.

Additional information can be found [here](https://wiki.unrealadmin.org/Category:UT2004)

## Getting Started with Game Servers in Docker

Credits again to LacledesLAN for the base image.

[Docker](https://docs.docker.com/) is an open-source project that bundles applications into lightweight, portable,
self-sufficient containers. For a crash course on running Dockerized game servers check out [Using Docker for Game
Servers](https://github.com/LacledesLAN/README.1ST/blob/master/GameServers/DockerAndGameServers.md). For tips, tricks,
and recommended tools for working with Laclede's LAN Dockerized game server repos see the guide for [Working with our
Game Server Repos](https://github.com/LacledesLAN/README.1ST/blob/master/GameServers/WorkingWithOurRepos.md). You can
also browse all of our other Dockerized game servers: [Laclede's LAN Game Servers
Directory](https://github.com/LacledesLAN/README.1ST/tree/master/GameServers).
