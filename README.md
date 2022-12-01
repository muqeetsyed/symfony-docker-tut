# symfony-docker-tut

<strong>Pre-Requisite:</strong>
Ensure uyou have installaed Docker Desktop locally.

Then clone the repository and rename the directory if u want.

Once done,
Go to the project directory and run <strong>docker-compose up -d --build</strong> in the terminal.
This will build the contianer in the Docker.

In order to create migration or add tools in which symfony application depends on, 
run <strong>docker-compose exec php /bin/bash</strong> in the terminal.

Create a .env.local file from the existing .env file
And now update the database parameters in .env.local to allow your application to connect to your database container.
<strong>DATABASE_URL="mysql://root:secret@database:3306/symfony_docker?serverVersion=8.0"</strong>





