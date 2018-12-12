# Getting started with SQL 2019 big data cluster in Azure

## What is SQL 2019 big data cluster?

SQL Server 2019 is in preview and will include Apache spark and Hadoop Distributed File System (HDFS). 
This new architecture of SQL 2019 that combines structured and unstructured data processing engines is called a big data cluster. 
You will find more details [here](https://docs.microsoft.com/en-us/sql/big-data-cluster/big-data-cluster-overview?view=sqlallproducts-allversions).

## Sign up for SQL 2019 big data cluster

Currently, to gain access to the images that form the crux of the SQL 2019 big data cluster, the customer will need to signing up [here](https://sqlservervnexteap.azurewebsites.net/). 
Once the SQL team approves your request, you will receive a user name and password that will provide access to the containers.

## Setting up a client machine in Azure to access the big data cluster

Go to the azure portal and create a VM with Windows operating. I use a Windows 10 pro, version 1803 to build my client VM in azure.

<p align="center">
  <img width=400 length=125 src='images/pic1.jpg'>
</p>

You can find details about how to create a virtual machine in azure [here](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/quick-create-portal). 
Once the validation is complete click on the “create” button to initiate the creation VM creation process.

<p align="center">
  <img width=400 length=125 src='images/pic2.jpg'>
</p>

## Install pre-requisites on the client machine (Azure VM)

To use AKS cluster, which is one of the many locations where SQL 2019 big data cluster can be installed, we will need to install [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/#install-kubectl) and mssqlctl CLI tool to 
manage SQL Server big data cluster. Python v3 (or greater) and pip3 are to be installed before installing mssqlctl.In addition to this, it will be good to 
install the [Azure Data Studio and SQL Server 2019 extension](https://docs.microsoft.com/en-us/sql/big-data-cluster/deploy-big-data-tools?view=sqlallproducts-allversions). 
If you intend to use Azure CLI to install AKS cluster, this will also need to be installed on the client machine that was created.

### Installing kubectl  

In the client machine open PowerShell window and paste the command

<table bgcolor="#D3D3D3">
<tr>
 <th><strong>Install-Script -Name install-kubectl -Scope CurrentUser -Force</strong></th>
</tr>
</table>
