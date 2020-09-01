## PAAS-TA-CUBRID-RELEASE   

### Notices     
  - Use PAAS-TA-CUBRID-RELEASE >= v.2.0.1    
    - PaaS-TA >= v.5.0.2    
    - service-deployment >= v5.0.2    
  - Use PAAS-TA-CUBRID-RELEASE =< v.2.0.0    
    - PaaS-TA =< v.5.0.1   
    - service-deployment =< v5.0.1    

### PaaS-TA Cubrid Release Configuration   

  - cubrid : 1 machine   
  - cubrid_broker : 1 machine   

### Create PaaS-TA Cubrid Release   
  - Download the latest PaaS-TA Cubrid Release   
    ```   
    $ git clone https://github.com/PaaS-TA/PAAS-TA-CUBRID-RELEASE.git   
    $ cd PAAS-TA-CUBRID-RELEASE   
    ```   
  - Download & Copy "source files" into the src directory   
    ```   
    ## download source files      
    $ wget -O src.zip http://45.248.73.44/index.php/s/iDEAaFxHqNeHEoF/download   

    ## unzip download source files   
    $ unzip src.zip   

    ## final src directory   
    src   
      ├── cli   
      │   └── cf-linux-amd64-6.10.0.tgz   
      ├── cubrid   
      │   └── CUBRID-10.2.1.8849-de852d6-Linux.x86_64.tar.gz   
      ├── cubrid_broker   
      │   └── openpaas-cf-service-java-broker-cubrid.jar   
      └── java   
          └── OpenJDK8U-jre_x64_linux_hotspot_8u212b03.tar.gz   
    ```    
  - Create PaaS-TA Cubrid Release    
    ```   
    ## <VERSION> :: release version (e.g. 2.0.1)   
    ## <RELEASE_TARBALL_PATH> :: release file path (e.g. /home/ubuntu/workspace/paasta-cubrid-<VERSION>.tgz)   
    $ bosh -e <bosh_name> create-release --name=paasta-cubrid --version=<VERSION> --tarball=<RELEASE_TARBALL_PATH> --force   
    ```    
### Deployment   
- https://github.com/PaaS-TA/service-deployment   
