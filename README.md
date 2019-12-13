Cloudwatch Exporter 

This repo contains config used to deploy prometheus-cloudwatch-exporter to openshift

## Usage
```
$ oc new-project cloudwatch-exporter
```
Update `cloudwatch-exporter-sec.yaml` with AWS credentials having `CloudWatchReadOnlyAccess` permissions.
```
$ oc apply -f cloudwatch-exporter
```
Install prometheus operator to `cloudwatch-exporter` namespace
```
$ oc apply -f prometheus
```
