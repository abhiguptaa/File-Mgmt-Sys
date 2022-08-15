
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
    storage name,

        miniprojectccdb 

    its region performance, redundancy. Once reviewed, a storage account will
    be created.
    To store files, we create **blob containers.**
- **Streamlit application**

    Streamlit is an open-source app framework for Machine Learning and Data Science teams.
    Create beautiful web apps in minutes. We use python scripts to build this application.
    The main functions are –
    - Uploading a file using Browse button    
    - Downloading a file using Download button
    - Displaying all the list of files uploaded in the download section.
    We get a connection string using Azure Blob. Using the string we upload a **file of .pdf type.**
    With the help of **Blob Client** the files have been uploaded/retrieved into/from the azure
    storage.The downloaded function consists of downloading a file as well as displaying all the files
    name stored using blob client.
- **Deploy the application using Paas**

    For deploying the application, we need to containerize the app using docker.
    Dockerfile is a text file which contains all the steps to be performed to create our application as
    a image.The base image i.e. python 3.8, all the related files to be copied, the sudo command to install
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


## Acknowledgements

 - https://docs.microsoft.com/en-us/azure/container-registry/container-registry-get-started-portal?tabs=azure-cli
 - https://docs.microsoft.com/en-us/azure/app-service/overview-hosting-plans
 - https://techcommunity.microsoft.com/t5/iis-support-blog/upload-and-download-files-from-azure-storage/ba-p/287834
 - https://azurelessons.com/upload-and-download-file-in-azure-blob-storage/
## Feedback

If you have any feedback, please reach out to us at abhigupta0031@gmail.com


## Screenshots



