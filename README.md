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
<img src="https://github.com/WojtekSza/Real_time_machine_learning/blob/main/Real_time_ml/1.jpg" alt="spark" width="400"/>  <br>

Next step is to attach compute cluster.
```
az ml compute create --name ml-cluster --size Standard_DS11_v2 --min-instances 1 --max-instances 2 --type AmlCompute --resource-group Realtimeml --workspace-name realtimeml
```
When compute cluster is ready then we can create machine learning model. <br>
As a example we will use tutorial of car price prediction
```
https://learn.microsoft.com/pl-pl/azure/machine-learning/tutorial-designer-automobile-price-train-score
```
When all steps in tutorial are completed then we can solve model and obtain following resutls<br>
<img src="https://github.com/WojtekSza/Real_time_machine_learning/blob/main/Real_time_ml/2.jpg" alt="spark" width="400"/>  <br>
<img src="https://github.com/WojtekSza/Real_time_machine_learning/blob/main/Real_time_ml/3.jpg" alt="spark" width="400"/>  <br>


Last step is to remove all created resources
```
az group delete --name Realtimeml
```
