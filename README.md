# serverless-demo

AIM of this repository is collect components for a 360' serverless experience with google cloud


## Google cloud Project
If you have not already created a GCP domain, register into google cloud and create a project.
Once the project is created you can connect to the cloud shell and obtain you project id:
`gcloud projects list`
along this project I'm assuming the default configured project will be the one generated for this step:
`gcloud config set project PROJECT_ID`
again every command listed will report PROJECT_ID, replace it with the one of your project.

## Domains
Since load balancer require a domain to be correctly configured I would like to start from a domain registration from google domains.
`https://console.cloud.google.com/net-services/domains/registrations/list?referrer=search&project=PROJECT_ID`
Create a new domain ( I've choosen a .dev domain ).

## Identity Aware Proxy
It let you to manage user access to Load balancer managed backends or App Engine, Compute Engine, GKE. It creates a central authorization layer for application accessed by HTTPS.
IAP uses a JWT Token to ensure you are authorized to access the application.

## Serverless VPC Access
You can use a Serverless VPC Access connector to connect your serverless environment directly to your Virtual Private Cloud (VPC) network, allowing access to Compute Engine virtual machine (VM) instances, Memorystore instances, and any other resources with an internal IP address.

1. abilitare le api cloud dns
2. registrare un dominio, nel mio caso a11dev.dev, registrato utilizzando il servizio di google domains `https://console.cloud.google.com/net-services/domains/registrations/create?project=PROJECT_ID`
