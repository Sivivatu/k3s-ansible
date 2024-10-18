

helm upgrade kestra kestra/kestra --namespace kestra --values ./values.yaml

# Deploy and update kestra
Deploying kestra is done using the helm chart as per the following [documentation](https://docs.kestra.com/deploying-kestra/)

## Install 

Installing the helm chart is completed after adding and updating the chart service, then installing the chart. 
This must be done from the deployments/kestra folder, otherwise the wrong values file will be applied

```bash
# install helm chart
helm repo add kestra https://helm.kestra.io/

# update all charts
helm repo update

#install kestra
helm install kestra kestra/kestra --namespace kestra --values ./values.yaml
```

## To update the chart
To upgrade the kestra version or change any values configuration this is done using the following command
This must be done from the deployments/kestra folder, otherwise the wrong values file will be applied

```bash
helm upgrade kestra kestra/kestra --namespace kestra --values ./values.yaml
```
