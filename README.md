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
DB_NAME="my_db"
DB_USER="db_user"
DB_PASSWORD="db_password"
DB_ROOT_PASSWORD="db_root_password"
# Enter your Domain or Subdomain here
WP_DOMAIN="mydomain.com"
```
4. Fire it up:
```
docker-compose up -d
```
