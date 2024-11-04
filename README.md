# pre-setup
make the following directory

```
mkdir /Users/boyouzho/dns-config
mkdir /Users/boyouzho/dns-config/passwords
mkdir /Users/boyouzho/dns-config/configs
```

# setup

Here are the commands to run the yml docker file.
```
docker compose up -d

docker compose down
docker image rm technitium/dns-server
docker compose up -d
```

# configure the local ip
add the line here to the file `/etc/hosts`

```
127.0.0.1	boyou.home.local
```

# change password
go to 127.0.0.1:5380 and then change the password for the dns server

# change to https
go to settings and enable https

# add dns over https
go to settings and go to optional protocals, enable dns-over-https

# add dns forwarders
enable cloudflare dns over https in "proxy & forwarders" under settings

# generate the certificate and add them inside the dns server

# upgrade

docker compose down
docker pull technitium/dns-server:latest
docker compose up -d
