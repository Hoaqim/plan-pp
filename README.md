# Plan zajec
---
## Specification
### Frontend
- Node 14.18.1
- ReactJS >=17.0.2

### Backend
- Python 3.9
- Django >= 3.0 , < 4.0
- Django rest framework ...

---
## Docker
[Download Docker](https://www.docker.com/get-started)

Build containers by typing in console:
```console
docker-compose build
```

To run our app type:
```console
docker-compose up
```

**EXTREMELY IMPORTANT!**

There is a file 'sample.env'. You need to create '.env' file in the same folder as 'sample.env'.
Just create a copy of the file, change its name to '.venv', then generate your secret key (you can use for example https://djecrety.ir) and change it into SECRET_KEY. You should also change DBUSER and DBPASSWORD into values you want.

---
## BACKEND

To execute Django commands inside your container use comand:
```console
docker exec -it backend-planpp python manage.py <command>
```
For example: to create Django super user type:
```console
docker exec -it backend-planpp python manage.py createsuperuser
```

## Migrations
Sometimes you will need to make migrations in Django server.
In order to do that, your Docker container must be enabled. After that type:
```console
docker exec -it backend-planpp python manage.py makemigrations
docker exec -it backend-planpp python manage.py 
```