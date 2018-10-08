# Rockons
A collection of some custom rockons i use on my rockstor nas



Look at the [official  repo](https://github.com/rockstor/rockon-registry) for details on installation.

## mosquitto
the official mosquitto image expect to have a conf file mounted not a folder, so to get this working it is required to place a conf file in the share you plan to mount. the file can be downloaded from [github](https://github.com/eclipse/mosquitto/blob/master/mosquitto.conf)

## TVheadend
this requires some changes to privileges for db devices see [this](https://forum.rockstor.com/t/hardware-permessions/1345) forum post for more info. (keep in mind the "code" section in the post uses pretty quotation marks so you have to replace those for the script to work)

## makemkv
you will have to change the two device options (sr0 and sg6) to fit your setup. i found the easiest way to find those values was by spinning a container up from the command line and read the logs as described in the [documentation](https://hub.docker.com/r/jlesage/makemkv/) for the container

## Steamcache
run both steamcache(must use port 80) and steamcache dns(must use port 53) and point the steamcache_ip to the steamcache rockon.
see https://hub.docker.com/u/steamcache/ for more info.
(steamcache -complete is currently not working)
