# Willbox

## System requirements
- Docker (ubuntu/mac)
- Docker-Desktop (windows)

## Docker Installation
- Clone this repository
```
git clone https://github.com/thynameisjayvee/willbox_docker.git <your-project-name>
```
- Copy environment configurations (go to your project directory and copy configuration file)
```
cd <your-project-name>
cp .env.example .env
```
- Modify environment configuration based on your needs(eg. database name, ports etc.)
- Build and Up Docker images
```
docker-compose up -d --build
```

## Laravel Installation
- navigate to docker php (from your project directory)
```
docker exec -it php-willbox sh
```
- Install laravel dependencies
```
composer install
```
- Setup laravel environment configuration
```
cp .env.example .env
```
- Modify environment configuration based on your needs(eg. database name, ports etc.)
- Install required laravel keys and migrate database
```
php artisan key:generate
php artisan migrate
```
## Install node modules
- Exit from Docker php sh
- navigate to docker node
- docker exec -it node-willbox sh
```
npm install or yarn install
```
- Build assets or watch
```
npm run watch or yarn run watch --to watch files during development
npm run prod or yarn run prod --for production server
```

## Browser
```
localhost:10080 --default
or
localhost:<your env WEB_PORT>
