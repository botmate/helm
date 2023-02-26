# BotMate Helm Charts

This repository contains the Helm charts for the BotMate platform.

## To make an update

### Step 1: Make changes in templates

Make changes in the templates. Make sure to update the `appVersion` field in the `Chart.yaml` file.

### Step 2: Update the chart version

- In the `Chart.yaml` file, update the `version` field.
- Run `helm lint` to make sure the chart is valid.
- Run `helm package` to package the chart.

### Step 3: Update the index

Run `helm repo index --url https://botmate.github.io/helm/ --merge index.yaml .` to update the index file.

### Step 4: Commit and push

Commit and push the changes to the repository.

## To install the chart

Run `helm repo add botmate https://botmate.github.io/helm/` to add the repository to Helm.

Run `helm install botmate/botmate` to install the chart.

## To uninstall the chart

Run `helm uninstall botmate` to uninstall the chart.
