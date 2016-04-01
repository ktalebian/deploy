# deploy
A simple bash script to run tests and deploy your code to a server and run docker. 

This script assumes you have `docker-compose` installed and that your application on the `docker-compose` configuration is named `application`. This script also assumes the following hierarchy:
    
    /
        deploy
        /application (or any other name)
            Dockerfile
            # All files related to application go here


## Setup
Update the file to include repo's and server's information. If your "application" is under a different name, then update the variable `APP_FOLDER_NAME`.

### Deployment:

To deploy with default setting:

    ./deploy        # Deploys dev branch to DEV_SERVER_IP
    ./deploy -p     # Deploys master branch to PROD_SERVER_IP

To deploy a different branch:

    ./deploy BRANCH_NAME       # Deploys BRANCH_NAME to DEV_SERVER_IP
    ./deploy -p BRANCH_NAME    # Deploys BRANCH_NAME to PROD_SERVER_IP