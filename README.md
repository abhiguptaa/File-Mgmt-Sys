
# File-Mgmt-Sys

To update, maintain, download files built Using Azure Service


## Demo

Insert gif or link to demo

https://drive.google.com/file/d/1Yl_U8tMFYybWZ7jXFkQWzogNIsEZLa18/view?usp=sharing
## About

The **File Management System** is used to upload, maintain download files in order to minimize
the number of hard copies on hand. Users will be able to manage their documents online as
part of this initiative. The features of the project are possibly inspired by Google Drive File
Management, with the exception that this framework would only concentrate on a single entity
or institution.
A file management system helps you to store, exchange, and maintain all of your
company’s/organization’s file records. This project’s functionality can be applied to colleges,
offices, or any other organization that wants to handle and store their file records using cloud
service




## Features

- **Upload** and **download files, documents, images, videos** through online in a secured manner.
- Files can be **downloaded/uploaded** in any file format.
- **Azure Blob Storage** to store file details
- **Azure Container Registry** to store the docker images
- **Azure App Services** for PaaS
- **Azure App Service** Plan for IaaS



## Deployment

- **Azure Service for Storage**

    The Azure Storage platform is Microsoft's cloud storage solution for modern data storage
    scenarios. Azure Storage offers highly available, massively scalable, durable, and secure
    storage for a variety of data objects in the cloud. Azure Storage data objects are accessible
    from anywhere in the world over HTTP or HTTPS via a REST API.
    As in our application, files have been stored, retrieved and downloaded, we use Azure Blob
    storage library.

    Azure Blob Storage is Microsoft's object storage solution for the cloud. Blob storage is
    optimized for storing massive amounts of unstructured data, such as text or binary data.
    Here, we create a storage account, input subscription, its resource group, 
    storage name,its region performance, redundancy. Once reviewed, a storage account will
    be created.

        miniprojectccdb 

    
    To store files, we create **blob containers.**
    ![image](https://user-images.githubusercontent.com/85796313/184662365-d3f039c9-f5b5-427c-9e20-0aa731befc23.png)
    
    ![image](https://user-images.githubusercontent.com/85796313/184662410-16c7ef1c-8103-4d2e-9047-77e5342d8169.png)
    

- **Streamlit application**

    Streamlit is an open-source app framework for Machine Learning and Data Science teams.
    Create beautiful web apps in minutes. We use python scripts to build this application.
    The main functions are –
    - Uploading a file using Browse button    
    - Downloading a file using Download button
    - Displaying all the list of files uploaded in the download section.
    
    ![image](https://user-images.githubusercontent.com/85796313/184662499-23cfb074-8013-47b2-bef9-9756abc77f27.png)

    We get a connection string using Azure Blob. Using the string we upload a **file of .pdf type.**
    With the help of **Blob Client** the files have been uploaded/retrieved into/from the azure
    storage.The downloaded function consists of downloading a file as well as displaying all the files
    name stored using blob client.
- **Deploy the application using Paas**

    For deploying the application, we need to containerize the app using docker.
    Dockerfile is a text file which contains all the steps to be performed to create our application as
    a image.
    ![image](https://user-images.githubusercontent.com/85796313/184662642-25d810e6-6f85-46a7-818d-e5e71d9806c3.png)
    
    ![image](https://user-images.githubusercontent.com/85796313/184662677-57212e46-dba9-4e91-bc90-ed954d5923e5.png)

    The base image i.e. python 3.8, all the related files to be copied, the sudo command to install
    streamlit, a requirement.txt file which contains all the details that our application need to be
    executed, a **port 8501** and the command to run streamlit main.py has been included into the
    docker file 
    - To create image

            docker build -t

    Now to push this into container registry of azure, we need to use container registry service of
    azure.
- **Azure Container Registry**
    
    Azure Container Registry is a private registry service for building, storing, and managing
    container images and related artifacts
    For creating a container registry, the following needs to be inputed,

    - **Subscription:** Select your valid Azure subscription where you want to create container registry.
    
    - **Resource group:** Select the resource group which you created in previous step.
    
    - **Registry name:** Name of your Azure Container registry to be created.
    
    - **Location:** The location where you want to create ACR (Keep same as the resource group
        Region).
    
    - **SKU:** Select the registry tier Basic. (Available are Basic, Standard, Premium)
    
    ![image](https://user-images.githubusercontent.com/85796313/184662768-5679edbf-0cdb-412d-a42f-98d8d6f2b8b5.png)
    Here we push the docker file into the particular ACR. 
 
    For deploying, Azure service plan is implemented. 
    An App Service plan defines a set of compute resources for a web app to run. The app service plan defines what specification of hardware your app runs on, 
    and how many servers you have. 
    Once we create the app service, deploy the image to Azure service. 
    Here Iaas is being implement as a virtual machine has been created. 
    ![image](https://user-images.githubusercontent.com/85796313/184662944-2a4668fc-c484-4208-9329-5635494b030a.png)
    
    
    ![image](https://user-images.githubusercontent.com/85796313/184662974-9d928d1d-f68d-4ace-87db-9f8ce9d7701a.png)
    The url mentioned specifies that our application has been hosted. 
    
    **The application:**
    
    ![image](https://user-images.githubusercontent.com/85796313/184663117-82bde89c-d5a9-4e98-9e98-614970ef96c3.png)
    
    ![image](https://user-images.githubusercontent.com/85796313/184663149-58673c26-97a1-4beb-be98-4ba6b3107a68.png)
    
    ![image](https://user-images.githubusercontent.com/85796313/184663175-4f9abbc6-e4b4-40b3-ab6b-e36a0fa65484.png)
    
    ![image](https://user-images.githubusercontent.com/85796313/184663202-b5067341-25e3-427f-a6b9-b4909def91b0.png)
    




## Acknowledgements

 - https://docs.microsoft.com/en-us/azure/container-registry/container-registry-get-started-portal?tabs=azure-cli
 - https://docs.microsoft.com/en-us/azure/app-service/overview-hosting-plans
 - https://techcommunity.microsoft.com/t5/iis-support-blog/upload-and-download-files-from-azure-storage/ba-p/287834
 - https://azurelessons.com/upload-and-download-file-in-azure-blob-storage/
## Feedback

If you have any feedback, please reach out to us at abhigupta0031@gmail.com






