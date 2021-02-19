# Helm Charts

Index of Data61 Helm charts.

## To install a chart from this repository


    helm repo add data61-hardbyte https://hardbyte.github.io/data61-charts
    
    helm repo update
    
    helm search repo data61-hardbyte
    
    helm install data61-hardbyte/entity-service [--values...]


## How this repo works

This repository has been configured in github to serve the `docs` folder.

Package each chart from the release tag of an upstream repository:

    helm package entity-service
    mv entity-service-x.y.z.tgz docs

Update the index:

    helm repo index docs --url https://hardbyte.github.io/data61-charts
    
The commit and push.

