# Description of the Pipeline

### Orbs install tools quickly
1. Creates the Node, ElasticBeanstalk, and AWS Orbs
2. Installs the three 

### Jobs act as groups of commands
1. Build Job
    1. Sets up the docker image
    2. Installs node version 14.15
    3. Installs yarn
    4. Complese the checkout code
    5. Sets up aws-cli 
    6. Installs the front-end dependencies 
    7. Installs the back-end (api) dependencies
    8. Runs lint on front-end
    9. Build's the front-end code
    10. Builds the back-end (api) code

2. Deploy 
    1. Sets ElasticBeanstalk up 
    2. Sets AWS-CLI up  
    3. Runs checkout
    4. Installs Dependencies for front-end and back-end api
    5. Builds front-end and back-end api
    6. Deploys front-end and back-end api
    

### Workflows specify the order to execute jobs
1. Run Build Job first 
2. Hold and wait for approval before moving to Deploy Job
3. Runs Deploy Job last only if hold got approval to move on