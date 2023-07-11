```
docker run -d --name=heimdall -e PUID=1000 -e PGID=1000 -e TZ=Etc/UTC -p 8787:80 -p 443:443 --restart unless-stopped lscr.io/linuxserver/heimdall:latest
```
