# isec6000-assignment1-task1
This repository contains the setup code and instructions for creating a Kubernetes cluster using Google Kubernetes Engine (GKE) as part of the ISEC6000 Secure DevOps assignment.

### Introduction
As a part of a cutting-edge technology team of an innovative company, I am responsible for designing, developing, and securing a modern e-commerce-application that promises to shape the landscape of online shopping we do. My journey begins with setting up the initial infrastructure for the project that includes creating a Kubernetes cluster on GKE (Google Kubernetes Engine) which provides us all the computing resources to host our application.
Following is the step-by-step documentation on how to create a cluster on GKE:
### Prerequisites:
1)	Ensure you have a Google Cloud account.
2)	Install the `gcloud` command-line tool'.
3)	Install `kubectl` for managing the cluster
   
### Step 1:
You can log in to your Google cloud console. If you don’t have one, you must create one and log in. Once you log in to the console.
### Step 2: 
You need to create a project. To create a project click `New Project` as shown in the screenshot below:
![image](https://github.com/dahalapaar/isec6000-assignment1-task1/assets/112838370/26511642-7f83-4c78-a6d3-ad0ab43efc38)
Once you click `New project`, you will be redirected to the new page. 
![image](https://github.com/dahalapaar/isec6000-assignment1-task1/assets/112838370/ef22c7ca-9c2a-40d1-8f81-990b400110f4)
 
Type your Project name relevant to your project and click `Create`. Once you create your project, you are good to go to create clusters for the project.
### Step 3:
I have created my project as `ecommerce`. Navigate to your project and click `Create` under Kubernetes Clusters.
![image](https://github.com/dahalapaar/isec6000-assignment1-task1/assets/112838370/b6f98b25-6173-454e-86a3-d808e5153a92)
Once you click `Create`, you will be redirected to the new page where you have to provide the configuration details of your project.
![image](https://github.com/dahalapaar/isec6000-assignment1-task1/assets/112838370/76710ac5-3f4d-472c-9ebf-2a0add38ec89)

Provide the name of your cluster and location too.
![image](https://github.com/dahalapaar/isec6000-assignment1-task1/assets/112838370/be44265e-02f1-47cd-838e-f57f1f7e0ae5)
 
I have created my cluster as `ecommerce-cluster` and selected `australia-southeast1-b` as a location.
### NOTE: While choosing a location while creating a cluster, it is very important to consider the factors such as costs, availability of services, network connectivity and so on.

 ![image](https://github.com/dahalapaar/isec6000-assignment1-task1/assets/112838370/44509967-ed1a-45a4-b6ae-b9ce2b24c7db)

You can choose the specific version of Kubernetes. I have selected the default one. You can also configure the machine type, number of nodes, and other settings for the node pool. These settings determine the capacity and resources of your cluster. Depending on your needs, you might have options for configuring advanced settings, such as automatic scaling, node auto-repair, and node auto-upgrades.
Click `Create` once you finish filling in the configuration details.
### Step 4:
After few minutes, your cluster will be ready.
YAAHOO, Your cluster is ready.
![image](https://github.com/dahalapaar/isec6000-assignment1-task1/assets/112838370/b521b287-bdf5-4eb4-9f3a-8d5cad6b2db2)

 
You can see my cluster and its configuration details in the screenshot above. 

Now we need to configure `Kubectl` which is a command-line tool for interacting with the Kubernetes cluster. Here’s how you can do it:
### Step 1: Install “Kubectl”
If you don't have `kubectl` installed already, you need to install it. The installation process can vary depending on your operating system. You can find installation instructions for various platforms here: https://kubernetes.io/docs/tasks/tools/install-kubectl/ 
### Step 2: Authenticate Kubectl with GKE
After you install Kubectl in your system, you need to authenticate it with the GKE to interact with the clusters. To authenticate:
Log in to your Google Cloud Console.
a)	In the left navigation menu, go to `Kubernetes Engine` > `Clusters.`
b)	Find the cluster you created and click on its name to open its details.
c)	At the top of the cluster details page, there is a `Connect button`. Click on it.
![image](https://github.com/dahalapaar/isec6000-assignment1-task1/assets/112838370/cedebc07-5797-48b1-8dfa-20921c3a4570)

d)	After clicking `Connect`, you'll see a pop-up dialog with a command that you need to run in your local terminal. This command includes the necessary configuration for `kubectl` to connect to your GKE cluster.
 ![image](https://github.com/dahalapaar/isec6000-assignment1-task1/assets/112838370/7042931f-aeb9-4bb0-a4e2-95540998b6a2)

### Step 3:
Copy the command from the pop-up dialog and paste it into your terminal.
### Step 4:
Once you run the command, your `kubectl` will be configured to work with your GKE cluster. You can verify this by running commands like:
 `kubectl get nodes`
Now, we are ready to use Kubectl to manage and interact with our clusters.


