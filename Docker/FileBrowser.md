```
sudo docker run -d \
    -v /srv/dev-disk-by-uuid-:/srv \
    -v /var/lib/filebrowser/database.db:/database.db \
    -v /var/lib/filebrowser/filebrowser.json:/filebrowser.json \
    -p 3670:80 \
    filebrowser/filebrowser
```
