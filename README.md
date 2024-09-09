# Jenkins-basics

If you encounter error at:
docker exec jenkins-blueocean cat /var/jenkins_home/secrets/initialAdminPassword

use this command to get the initial password:
docker logs jenkins-blueocean
