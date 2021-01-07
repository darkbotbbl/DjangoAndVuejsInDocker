# DjangoAndVuejsInDocker
Dockerfiles and docker-compose files for how to set up a django and vuejs project together in docker. There are both setups for production and development stages of the project. 

Tech Stack 
Django
Vue.js 
Nginx
Docker
Posgresql
Redis

Of course not all of these are going to be used in project, but they 
are included anyway. Feel free to adjust them to fit your use case. 

## Development
### Django
In the dockerifle of the backend or django as used here, pipenv is used to install the python packages. 
A default entrypoint.sh file was added, this is so as to allow us to add a bash code to ensure we are able to monitor the database service's status and only start the backend service when the database service is running since the backend depends on it.

Also please make the entrypoint.sh file executable before running docker-compose build.
Run chmod +x entrypoint.sh in your terminal to make the bash script executable.


