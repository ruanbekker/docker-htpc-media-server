# docker-htpc-media-server
HTPC with Docker Compose

## Configuration

### Disks

My disks are structured like this:

```
$ df -h
Filesystem      Size  Used Avail Use% Mounted on
/dev/sdd1       1.4T  364G  940G  28% /
mergerfs        9.1T  8.8T  124G  99% /data
/dev/sdb1       1.9T  1.8T   34G  99% /disk1
/dev/sdc1       1.9T  1.8T   34G  99% /disk2
/dev/sdf1       1.9T  1.8T   23G  99% /disk3
/dev/sda        3.6T  3.4T   35G 100% /disk4
```

- `MERGERFS_ROOT=/data/htpc` - this is my mergerfs volume which is configured on /disk* (all downloads resides there)
- `CONFIG_ROOT=/disk1/htpc`  - this is where all my config resides on and wanted it on one disk only
- `DOCKER_ROOT=/disk2/docker-volumes` - volume for all my docker containers, wanted it on one disk only
- `SSD_ROOT=/home/htpc/.data` - this is for most cached items, i wanted this to be on my local disk
