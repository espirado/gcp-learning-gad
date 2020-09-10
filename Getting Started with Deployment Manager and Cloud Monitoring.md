### Creating a deployment using Deployment Manager and use it to maintain a consistent state of your deployment.
#### Activate the following Apis
  ##### 
         - Cloud Deployment Manager v2 API

        -  Cloud Runtime Configuration API

        -  Cloud Monitoring API

###  On your terminal 

   ##### connect to instance
   
         - gcloud auth login --no-launch-browser
         - gcloud config set project PROJECT_ID
         - export MY_ZONE=
         - export MY_ZONE=us-central1-a
         - gsutil cp gs://cloud-training/gcpfcoreinfra/mydeploy.yaml mydeploy.yaml
         - sed -i -e "s/PROJECT_ID/$DEVSHELL_PROJECT_ID/" mydeploy.yaml
         - sed -i -e "s/ZONE/$MY_ZONE/" mydeploy.yaml
         - gcloud deployment-manager deployments create my-first-depl --config mydeploy.yaml
         - nano mydeploy.yaml
         - add vale and save = value: "apt-get update; apt-get install nginx-light -y"
         - gcloud deployment-manager deployments update my-first-depl --config mydeploy.yaml
   ##### ssh into vm 
          - dd if=/dev/urandom | gzip -9 >> /dev/null &
          
   ##### Check your monitor in the console
     
