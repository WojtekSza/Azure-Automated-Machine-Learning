# Real_time_machine_learning
Repository of real time machine learning created in Azure Machine Learning tool <br>
First step is to log into Azure CLI. Use following link to dowloand latest CLI package.
```
https://learn.microsoft.com/pl-PL/cli/azure/install-azure-cli-windows?tabs=azure-cli
```
```
az login
```
After sucesfull authentication next step is to create Azure resource group
```
az group create -l francecentral -n Realtimeml
```
Next step is to create Azure Machine Learning workspace.<br>
Use following link to install ml extension.
```
az extension add -n ml -y
```
```
az ml workspace create --resource-group Realtimeml --location francecentral --name realtimeml
```
After sucessfull workspace creation you should be able to log in into portal <br>
<img src="https://github.com/WojtekSza/Real_time_machine_learning/blob/main/Real_time_ml/1.jpg" alt="spark" width="400"/> 
