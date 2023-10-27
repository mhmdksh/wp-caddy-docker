# Wordpress with Caddy
Run wordpress with docker-compose and Caddy in 1 minute :p
## Prerequisites
1. Docker
2. Docker-Compose
3. Create a DNS **A record** to your servers Public IP Address
## How to run
1. Clone the repo:
```
git clone https://github.com/mhmdksh/wp-caddy-docker.git
```
2. Create and Customize your own ENV:
```
cp .env.template .env
```
3. Modify these values to your liking:
```
## Change this for External Database ##
DB_HOST="mysql"
DB_PORT="3306"

## Define Your DB Connection details here
DB_NAME="my_db"
DB_USER="db_user"
DB_PASSWORD="db_password"
DB_ROOT_PASSWORD="db_root_password"

## Specify your domains name here, Enter without http, or https
## Make sure the A records in your DNS Settings point to that server
WP_DOMAIN="mydomain.com"
DB_DOMAIN="db.mydomain.com"

## Specify the IP Addresses that are allowed to access the phpmyadmin page
IP_WHITELIST="IP1 IP2 IP3"
```
4. Fire it up:
```
docker-compose up -d
```
