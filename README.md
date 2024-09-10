# Jenkins-basics
Installation:
https://www.jenkins.io/doc/book/installing/


If you encounter error at:
docker exec jenkins-blueocean cat /var/jenkins_home/secrets/initialAdminPassword

use this command to get the initial password:
docker logs jenkins-blueocean

alpine/socat container to forward traffic from Jenkins to Docker Desktop on Host Machine:
https://stackoverflow.com/questions/47709208/how-to-find-docker-host-uri-to-be-used-in-jenkins-docker-plugin
Command1: docker run -d --restart=always -p 127.0.0.1:2376:2375 --network jenkins -v /var/run/docker.sock:/var/run/docker.sock alpine/socat tcp-listen:2375,fork,reuseaddr unix-connect:/var/run/docker.sock
Command2: docker inspect <container_id> | grep IPAddress 
