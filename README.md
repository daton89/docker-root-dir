# docker-root-dir
Change the default root dir folder ‘/var/lib/docker’ to another partition with more space

```sh
cd /etc/docker 
touch daemon.json
vim daemon.json
```

```json
// daemon.json file
{
    "graph": "/storage/docker-data",
    "storage-driver": "overlay",
    "hosts": ["tcp://127.0.0.1:4243", "unix:///var/run/docker.sock"]

}

```
