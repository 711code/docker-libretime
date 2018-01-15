# DOCKER Container for running libretime (www.libretime.org)

# How to run 
Run the following in a bash terminal:

mkdir -p ~/libretime/stor
mkdir -p ~/libretime/watch
mkdir -p ~/libretime/etc
mkdir -p ~/libretime/postgresql
docker run -d --restart=always -h libretime --name libretime -v ~/libretime/stor:/srv/airtime/stor -v ~libretime/watch:/srv/airtime/watch -v ~/srv/libretime/etc:/etc/airtime -v ~/libretime/postgresql:/var/lib/postgresql -p 80:80 -p 8000:8000 -p 20000:10000 johnnyc1951/docker-libretime

For persistence the container will mount libretime's folders in your home/libretime folder
 /etc/airtime
 /var/lib/postgresql
 /srv/airtime/stor
 /srv/airtime/watch

If not given, all will be kept into the container

# Attention!!!
System contains default passwords.
Please change /etc/icecast2/icecast.xml

# Installation
 after starting the container, wait ~30 sec to give the system
 the change to come up
 Connect to the container, created with the above command via Web
 make your 1st time parametration 
 restart your container 
 Ready .. to transmit
