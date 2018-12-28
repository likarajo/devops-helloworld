# devops

1. Pull Jenkins docker image and run it
* `$ docker pull jenkins`  
`Using default tag: latest`  
`latest: Pulling from library/jenkins`  
`Status: Downloaded newer image for jenkins:latest`
* `$ docker run -u root --rm -d -p 8080:8080 -p 50000:50000 \`  
`-v jenkins-data:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock jenkins`  
`b39e0ace38a0a1a92d6c02dbc61ca6ac6b0977e02cdbb8bc3f98284d6d6f6d71`  
* Jenkins initial setup is required using an admin user created and a password generated   
which can be found at: /var/jenkins_home/secrets/initialAdminPassword  
* `$ docker ps`  
`CONTAINER ID        IMAGE               COMMAND                        PORTS`  
`b39e0ace38a0        jenkins             "/bin/tini -- /usr/l…"   0.0.0.0:8080->8080/tcp, 0.0.0.0:50000->50000/tcp`
* Using the Ip and port, open the Jenkins page in web browser    
`https://0.0.0.0:8080`
2.
