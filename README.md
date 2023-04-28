# Lab_install_jenkins101
#1 * Before execute this command will need docker installed 
*  -d meand to run command in background
* Should access to a folder that docker-compose file located
docker-compose up -d

#2 * To access running docker container as a root user
docker exec -it -u root workshop_jenkins bash

#3 * To download AWS CLI insะall package, extract zip file and install package
curl "https:* awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" &&
unzip awscliv2.zip &&
./aws/install

#3  curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

#4 * Install docker in container
apt-get update && \
apt-get -y install apt-transport-https \
ca-certificates \
curl \
gnupg2 \
software-properties-common && \
curl -fsSL https:* download.docker.com/linux/$(. /etc/os-release; echo "$ID")/gpg > /tmp/dkey; apt-key add /tmp/dkey && \
add-apt-repository \
"deb [arch=amd64] https:* download.docker.com/linux/$(. /etc/os-release; echo "$ID") \
stable" && \
apt-get update && \
apt-get -y install docker-ce

#5 * To access Jenkins initial password
​​cat /var/jenkins_home/secrets/initialAdminPassword

------------------------------------------------------------------
