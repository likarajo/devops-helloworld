# devops
1. Create maven web project
* `$ mvn archetype:generate -DgroupId=io.github.likarajo -DartifactId=helloworld -DarchetypeArtifactId=maven-archetype-webapp`
* push the project files to Git repository

2. Pull Tomcat docker image and run it
* `$ docker run -it --rm -p 8888:8080 tomcat:8.0`
* `$ docker ps`  
`CONTAINER ID        IMAGE          PORTS`  
`b39e0ace38a0        tomcat:8.0     0.0.0.0:8888->8080/tcp`

3. Pull Jenkins docker image and run it
* `$ docker run -it --rm -p 8080:8080 jenkins`    
* `$ docker ps`  
`CONTAINER ID        IMAGE         PORTS`  
`b39e0ace38a0        jenkins       0.0.0.0:8080->8080/tcp, 0.0.0.0:50000->50000/tcp`
* Using the IP and port, open the Jenkins page in web browser    
`https://0.0.0.0:8080`
* Jenkins initial setup is required using an admin user created and a password generated   
which can be found at: /var/jenkins_home/secrets/initialAdminPassword OR by `$docker logs <container id>`

