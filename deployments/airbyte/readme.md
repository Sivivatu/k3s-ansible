# Deploy and update airbyte
Deploying airbyte is done using the helm chart as per the following [documentation](https://docs.airbyte.com/deploying-airbyte/)

## Install 

Installing the helm chart is completed after adding and updating the chart service, then installing the chart. 
This must be done from the deployments/airbyte folder, otherwise the wrong values file will be applied

```bash
# install helm chart
helm repo add airbyte https://airbytehq.github.io/helm-charts

# update all charts
helm repo update

#install airbyte
helm install airbyte airbyte/airbyte --namespace airbyte --values ./values.yaml
```

## To update the chart
To upgrade the airbyte version or change any values configuration this is done using the following command
This must be done from the deployments/airbyte folder, otherwise the wrong values file will be applied

```bash
helm upgrade airbyte airbyte/airbyte --namespace airbyte --values ./values.yaml
```
