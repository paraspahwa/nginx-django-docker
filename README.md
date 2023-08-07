# Simple Notes App
This is a simple notes app built with React and Django.

## Requirements
1. Python 3.9
2. Node.js
3. React

## Installation
1. Clone the repository
```
git clone https://github.com/LondheShubham153/django-notes-app.git
```

2. Build the app
```
docker build -t notes-app .
```

3. Run the app
```
docker run -d -p 8000:8000 notes-app:latest
```

## Nginx

Install Nginx reverse proxy to make this application available

`sudo apt-get update`
`sudo apt install nginx`

## If you want to know step by step coding please refer from here:

nginx is web server used for serving static web files it also acts like a reverse proxy , load balancing , URL redirection , indexing , caching .

local host : 127.0.0.1/8000

Nginx works on port 8080



create a a new instance with ubuntu ( allow http and https)

`sudo apt-get update -y`

`sudo apt install nginx -y`

`systemctl status nginx && systemctl start nginx && systemctl enable nginx && systemctl restart nginx`

also check by using public IP

`d /var/www/html`

`cd /etc/nginx/`

configuration file : nginx.conf -- has all the information for configuration
sites-available - configurtion available  - it will not work
sites-enabled - configuration enabled - it will work

check if app is working on local and get the code from github : 
git clone https://github.com/LondheShubham153/django-notes-app.git

`cd django-notes-app/`

`sudo apt install docker.io`

# Give permission to user command : 

`sudo usermod -aG docker $USER`
`sudo reboot`

`docker build -t notes-app .`

`docker run -d -p 8000:8000 notes-app:latest`

to check if app is working on local host :

`curl -L http://127.0.0.1:8000`

to check if backend is working or not : 

`curl -L http://127.0.0.1:8000/api`

adding proxy pass in the file : 
`cd /etc/nginx/sites-enabled/default`

proxy_pass http://127.0.0.1:8000;

location /api

proxy_pass http://127.0.0.1:8000/api;

copy the build/static file in to var/www/html
`sudo cp -r * /var/www/html/`


happy codeing !!!!!



