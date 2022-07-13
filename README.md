# Owncloud
Docker compose setup file for owncloud server with jwilder reverse proxt


## Install

Run 

```shell
cat << EOF > .env
OWNCLOUD_VERSION=10.10
OWNCLOUD_DOMAIN=localhost:8080
ADMIN_USERNAME=admin
ADMIN_PASSWORD=admin
HTTP_PORT=8080
EOF
```

Open `.env` and edit. With jwilder reverse nginx proxy `OWNCLOUD_DOMAIN` shoule be set to your domain/subdomain.
You can generate a `ADMIN_PASSWORD` with command "echo `date` | md5sum" 

Then run

```shell
docker-compose up -d
```

Done!
