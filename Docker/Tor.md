[link](https://hub.docker.com/r/kasmweb/tor-browser#!#)

`docker run --rm -d --shm-size=512m -p 6901:6901 -e VNC_PW=password kasmweb/tor-browser:1.13.0`

# Copy folder from docker
`docker cp -a e777aab1e163:/home/kasm-user/Desktop/Downloads/. c:\Users\xyz\Documents\images\`
where `e777aab1e163` is the hash of the container
