# Jenkins_project

### [Install Jenkins in Ubuntu](https://github.com/AshokTippaluri/Jenkins_project/blob/main/Jenkins.sh)

``` bash
#!/bin/bash

sudo apt update -y

sudo apt upgrade -y 

sudo apt install openjdk-17-jre -y

curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update -y 
sudo apt-get install jenkins -y

systemctl start jenkins
systemctl status jenkins
````
Hurray !! Now you can access the ```Jenkins``` Server on ``http://<ip-address>:8080``

![image](https://github.com/AshokTippaluri/Jenkins_project/assets/96752472/8a93a1a7-7d52-4a43-940a-468b83e9805b)

enter the ```initialAdminPassword``` we can find in the  sudo /var/lib/jenkins/secrets/initialAdminPassword

```sudo cat /var/lib/jenkins/secrets/initialAdminPassword ```

Click on the suggest plugins

![image](https://github.com/AshokTippaluri/Jenkins_project/assets/96752472/f41bc35e-7d4b-4b23-b976-3ef397c09888)

![image](https://github.com/AshokTippaluri/Jenkins_project/assets/96752472/e6b2f03d-41d2-4eaa-b4c7-63365756e042)

![image](https://github.com/AshokTippaluri/Jenkins_project/assets/96752472/f5257839-cdb1-47cd-8af6-aa26ed420f58)
![image](https://github.com/AshokTippaluri/Jenkins_project/assets/96752472/eedf9dff-99bf-47a8-8836-9e4ae86c119f)

![image](https://github.com/AshokTippaluri/Jenkins_project/assets/96752472/938aa9e0-8f29-48d0-a2c5-5eb9867e408e)


``` bash
apt install unzip
adduser sonarqube
wget https://binaries.sonarsource.com/Distribution/sonarqube/sonarqube-9.4.0.54424.zip
unzip *
chmod -R 755 /home/sonarqube/sonarqube-9.4.0.54424
chown -R sonarqube:sonarqube /home/sonarqube/sonarqube-9.4.0.54424
cd sonarqube-9.4.0.54424/bin/linux-x86-64/
./sonar.sh start
```
Hurray !! Now you can access the ```SonarQube``` Server on ```http://<ip-address>:9000```





