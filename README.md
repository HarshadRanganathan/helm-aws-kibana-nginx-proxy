# helm-aws-kibana-nginx-proxy
Helm chart for installing proxy for AWS Managed Kibana service

## Install/Upgrade Chart

Sample command to install/upgrade chart.

```
helm upgrade -i kibana-nginx-proxy . -n platform --values stages/shared-values.yaml --values stages/prod/prod-values.yaml
```
