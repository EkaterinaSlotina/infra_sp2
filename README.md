# infra_sp2                                                                                 

This is basic prject to practis how to launch django using docker and docker-compose

To launch the project you need to create **.env** file
**.env** file tempate should be structured like
>DB_ENGINE=django.db.backends.postgresql
>DB_NAME={your_database}
>POSTGRES_USER={database_username}
>POSTGRES_PASSWORD={databes_password}
>DB_HOST=db
>DB_PORT={database_port}

## First launch
To launch the project you need to execut this command in your terminal:
>docker-compose up --build -d 

If you launch the project for the first time, you need to execute this command after launching docker-compose to fulfill basic requirements of the django project:
>docker-compose exec web python manage.py migrate --noinput 
>docker-compose exec web python manage.py createsuperuser 
>docker-compose exec web python manage.py collectstatic --no-input


