Do katalogu .ssh trzeba dodać klucze, potrzebne do połączenia z gitem ;)

First build the container and give a name to the resulting image:
`docker build -t jenkins/android .`
 
Run in background:
`docker run -d -P --name android_project_name jenkins/android`
 
You can start an interactive session to test new commands with:
`docker runt -P jenkins/android /bin/bash`
 

Configure docker container as jenkins node.
 
Check IP address:
`docker inspect --format '{{ .NetworkSettings.Gateway }}' android_project_name`
 
Check port:
`docker port android_project_name 22`