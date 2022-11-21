# spring-gumball
## CI Workflow
### Using the Gradle starter workflow
On GitHub, go to Action and click on create new workflow, then find java with gradle to create file gradle.yaml.
Gradle workflow is successfully created and shown in the directory
![](images/1.png)

Images below shown the workflow is created successfully
![](images/2.png)

![](images/3.png)

![](images/4.png)

## CD Workflow
### Deploying to Google Kubernetes Engine
#### Creating a GKE cluster
Go to google console -> Kubernetes Engine -> Cluster to create new cluster.
Configure Standard cluster
![](images/create-cluster1.png)
Name of the cluster is cmpe172
Zone i sus-central-c
![](images/create-cluster2.png)
New cluster is creating
![](images/create-cluster3.png)

#### Enabling the APIs
In Google Cloud Console -> click on APIs & service -> Library -> Private APIS to enable access APIs.
![](images/enable-api1.png)

![](images/enable-api2.png)

### Set up Secrets in Workspace
Find the Project ID by go to the dashboard 
![](images/set-up-secret1.png)
Project ID is under project info
![](images/set-up-secret2.png)

### Create a Service Account for GitHub Access
Click on Navigation -> IAM & Admin -> Service Accounts to create a new Service Account.
Service account name is spring-gumball
![](images/create-service-account1.png)
New service account is created
![](images/create-service-account2.png)
Go to Navigation ->  IAM & Admin -> IAM -> Permissions to grant access 
![](images/grant-access1.png)
Enter the principals name
![](images/grant-access2.png)
Enter roles
![](images/grant-access3.png)
Access is granted
![](images/grant-access4.png)

#### Create a JSON service account key Links to an external site.for the service account
Go to Navigation ->  IAM & Admin -> IAM -> Service Account -> Select "spring-gumball" -> Keys -> Create New Key
![](images/service-account-key1.png)
Select Json
![](images/service-account-key2.png)
Download Json key file
![](images/json-key.png)
Json is created
![](images/json-key2.png)

#### Configure GitHub Secrets
On GitHub, go to 
![](images/gke-project.png)

![](images/gke-project2.png)

![](images/gke-sa-key.png)

![](images/gke-sa-key2.png)

#### Configuring Kustomize

![](images/configure-customize.png)

#### Trigger and Deployment to GKE

![](images/cluster1.png)

![](images/release.png)

![](images/release2.png)

![](images/release3.png)

![](images/workflow.png)

![](images/service-ingress.png)

![](images/create-ingress1.png)

![](images/create-ingress2.png)

![](images/web-ui.png)






