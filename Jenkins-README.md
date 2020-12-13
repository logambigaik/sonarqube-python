# Pre-Requisites:
    - Install Java
    - Install Git
    - Install Jenkins
    - Install sonarqube
    - Install sonar-scanner
# Install Jenkins
    sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins.io/redhat-stable/jenkins.repo
    sudo rpm --import http://pkg.jenkins.io/redhat-stable/jenkins.io.key
    sudo yum install jenkins -y
    service jenkins start
# Sonarqube installation
  [Sonarqube installaton](https://github.com/Naresh240/sonarqube-installation.git)
# Instll sonar-scanner
    cd /opt
    wget https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-4.4.0.2170-linux.zip
    unzip sonar-scanner-cli-4.4.0.2170-linux.zip
