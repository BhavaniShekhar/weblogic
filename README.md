# weblogic - DevOps lab activity
The objective of this project is to install the Weblogic in a Continuous Integration and Continuous delivery mode. In this WebLogic Installation and Configuration are automated with Shell and WLST scripts.

Step 1: First create a Weblogic Installation job in Jenkins using the Weblogic Installation.sh script given in this git source repository.
Note : this job should have 2 string parameters - `FMW_VERSION` and `BASE_HOME` (where installation should happen)

Step 2: Configure a domain using a Python script file - DomainCreation_Properties.py and In Jenkins you have to create a "OPENSTYLE" job with below set of commands and note that without any parameters-

    . $HOME/.bash_profile
    rm -rf weblogic
    git clone https://github.com/adis2hope/weblogic.git

    cd weblogic
    wlst DomainCreation_Properties.py

Step 3: If AdminServer not yet started then start admin server and add managed server followed by deployment process.
