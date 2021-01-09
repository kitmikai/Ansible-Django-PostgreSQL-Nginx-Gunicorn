# Ansible-Django-PostgreSQL-Nginx-Gunicorn

* Clone the repository
* cd into folder
* run command vagrant up
## When it has finished, it will display errors, continue with the database section below first.
* This section will be included in ansible in the next version
## Database
* vagrant ssh
* sudo -u postgres psql
* CREATE DATABASE myproject;
* CREATE USER myprojectuser WITH PASSWORD 'password';
* ALTER ROLE myprojectuser SET client_encoding TO 'utf8';
* ALTER ROLE myprojectuser SET default_transaction_isolation TO 'read committed';
* ALTER ROLE myprojectuser SET timezone TO 'Africa/Nairobi';
* GRANT ALL PRIVILEGES ON DATABASE myproject TO myprojectuser;
* \q

## Continue
* Run the command vagrant provision devserver
* Create and configure a new Django project using this tutorial (https://www.digitalocean.com/community/tutorials/how-to-set-up-django-with-postgres-nginx-and-gunicorn-on-ubuntu-20-04)