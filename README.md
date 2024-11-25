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
DB_NAME="wp_db"
DB_USER="wp_user"
DB_PASSWORD="wp_P@ssw0rd"
DB_ROOT_PASSWORD="wp_root_P@ssw0rd"

## Specify your domains name here. NOTE: Use `https://` prefix if you pointed the domain to the server
## or `http://` if you haven't pointed the domain or you are using this locally
WP_DOMAIN="http://mydomain.com"
DB_DOMAIN="http://db.mydomain.com"

## Specify the IP Addresses that are allowed to access the phpmyadmin page
IP_WHITELIST="127.0.0.1 10.0.0.0/8 192.168.0.0/16 172.0.0.0/8"
```
4. (Optional) Modify the php.ini configuration file under `./php/php_extras.ini` if needed:
```
file_uploads = On
memory_limit = 256M
upload_max_filesize = 256M
post_max_size = 256M
max_execution_time = 300
```
5. Fire it up:
```
docker-compose up -d
```
