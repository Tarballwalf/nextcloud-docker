### This is mainly for me (in case I fuck it up) not an actual tutorial for deploying Nextcloud 

Replace `EMAIL_HERE` and `DOMAIN_HERE` with the respective values

Create the docker network with 
```
# docker network create nextcloud_network
```

Now run the docker compose
```
# docker-compose up -d
```

Add the `custom_proxy.conf` to `$HOME/proxy/conf.d/`

Edit `config.pfp` (found in `$HOME/app/config/`) and add the following thing line (should be added at line 31, fixed the Nextcloud mobile app login loop)
```
'overwriteprotocol' => 'https',
```