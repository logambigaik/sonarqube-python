# sonarqube-python

# Pre-Requisites:
    - Install python, pip
    - Install nose, coverage, nosexcover, pylint
    - SonarQube Setup
    - Install Sonar-Scanar
# Install python and pip
    yum install python python-pip
# Install nose, coverage, nosexcover, pylint
    pip install nose coverage nosexcover pylint
## Sonarqube installation
   [Sonarqube installaton](https://github.com/Naresh240/sonarqube-installation.git)
# Clone code into local(/root)
    git clone https://github.com/Naresh240/sonarqube-python.git
    cd sonarqube-python
# Run command to get "nosetests.xml" & "coverage.xml"
  Once installed, you need to execute nosetests to run your unit tests, and generate information relating to the source code. The following line runs the test runner, generates coverage information, and generates an XML test report that SonarScanner will use:
    
    nosetests -sv --with-xunit --xunit-file=nosetests.xml --with-xcoverage --xcoverage-file=coverage.xml
  ![image](https://user-images.githubusercontent.com/58024415/102007246-569f7900-3d4d-11eb-91d7-220529dc18e1.png)
# Install Sonar-Scanar
    cd /opt
    wget https://binaries.sonarsource.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-4.4.0.2170-linux.zip
    unzip sonar-scanner-cli-4.4.0.2170-linux.zip
    mv sonarqube-python/sonar-scanner.properties /opt/sonar-scanner-4.4.0.2170-linux/conf/sonar-scanner.properties
#Copy test case folder into bin using cp
    
    [root@ip-172-31-5-148 my_sum]# cd /opt/sonar-scanner-4.4.0.2170-linux/bin
    [root@ip-172-31-5-148 bin]# mkdir my_sum
    [root@ip-172-31-5-148 bin]# cp /root/sonarqube-python/my_sum/__init__.py  /opt/sonar-scanner-4.4.0.2170-linux/bin/my_sum

 ![Capture](https://user-images.githubusercontent.com/54719289/105101172-77898580-5ad4-11eb-98a7-abd69d3db97d.JPG)


    
# Run Sonar-Scanar to test python application with SonarQube
    cd /opt/sonar-scanner-cli-4.4.0.2170-linux/bin
    ./sonar-scanner
  ![image](https://user-images.githubusercontent.com/58024415/102007223-1e983600-3d4d-11eb-9f60-6a5f313fc797.png)
# Check test result in Sonarqube UI 
 ![Capture](https://user-images.githubusercontent.com/54719289/105101004-385b3480-5ad4-11eb-8766-64379224417e.JPG)
