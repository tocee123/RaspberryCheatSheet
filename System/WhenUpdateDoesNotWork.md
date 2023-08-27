# When you got error `apt-get update` fail
[link](https://askubuntu.com/questions/1389758/apt-get-update-fails-due-to-no-pubkey-6af7f09730b3f0a4)
```
Err:7 https://apt.kitware.com/ubuntu bionic InRelease
The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 6AF7F09730B3F0A4
Fetched 11.0 kB in 1s (7552 B/s)
```
# Use the following command
`sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys [key]`
