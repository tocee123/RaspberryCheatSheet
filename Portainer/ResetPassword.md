```
sudo su
docker container stop portainer
docker run --rm -v portainer_data:/data portainer/helper-reset-password
docker container start portainer
```
[link](https://www.youtube.com/watch?v=A5ckT7pxrNY&list=PLhMI0SExGwfDsoRxRuDeOPPAfedcXFYSZ&ab_channel=DBTech) to youtube videos
