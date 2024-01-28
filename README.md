# HallowEthicalHacking

Soup (Knowledge Base)  
Watch (Security/Technology Watch)  
Pentest (Penetration Testing Helper)  
Writeup (Report Creator)  

## Clone Repository
```
$ git clone --recursive https://github.com/Ky7az/hallow-ethical-hacking
```

## Create Environment Files
Create `.env` file here
```
DOMAIN=your_domain_name
EMAIL=your_email
POSTGRES_USER=your_db_user
POSTGRES_PASSWORD=your_db_password
POSTGRES_DB=your_db_name
```

Create `.env` file into *django-hallow-ethical-hacking*
```
DEBUG=False
SECRET_KEY=your_secret_key
ALLOWED_HOSTS=your_domain_name
DB_ENGINE=django.db.backends.postgresql
DB_DATABASE=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_HOST=db
DB_PORT=5432
REDIS_URL=redis://redis:6379
```

## Update Domain Name
Edit `nginx/hallow.conf`, change the `server_name` directive with your domain name.  
Edit `vue-hallow-ethical-hacking/src/storage/service.js`, change the `API_HOST` const with your domain name.


## Build/Run Containers

### Traefik
```
$ cd trafik
$ docker network create proxy
$ docker compose up -d --build
```

### Hallow
```
$ docker compose up -d --build
```

## Create Superuser
```
$ docker exec -it django /bin/sh
$ python3 manage.py createsuperuser
```

## Shortcuts
```
Ctrl-E : Edit/Preview (Soup, Writeup)  
Ctrl-C : Copy (Pentest)
```

## Todo
- Update Django to next LTS version (4.2)
- Update Vue.js to next LTS version (3.4.x)
- Update Node.js to next LTS version (20.11.x)
- Add support to more watch sources
- Add more preconfigured pentest actions/commands
- Better handle exceptions/errors on frontend