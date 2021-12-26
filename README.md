# helm-aws-kibana-nginx-proxy
Helm chart for installing proxy for AWS Managed Kibana service

## Config Updates
In `prod-values.yaml` file available inside stages/prod folder, add values for below settings:

| | |
|--|--|
|hostname |Hostname to match for Ingress rule |
|alb.ingress.kubernetes.io/certificate-arn | ACM cert ARN for TLS connections |
|alb.ingress.kubernetes.io/load-balancer-attributes |S3 bucket to store LB Access logs |
|<vpc_domain> |Substitute with ES VPC Domain URL |

## Install/Upgrade Chart

Sample command to install/upgrade chart.

```
helm upgrade -i kibana-nginx-proxy . -n platform --values stages/shared-values.yaml --values stages/prod/prod-values.yaml
```
