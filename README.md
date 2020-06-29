# Moved

Please use repository on new URL : https://github.com/AckeeCZ/terraform-gcp-elasticsearch

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.12 |
| google | ~> 2.20.0 |
| google-beta | ~> 3.6 |

## Providers

| Name | Version |
|------|---------|
| google | ~> 2.20.0 |
| kubernetes | n/a |
| tls | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| cluster\_ipv4\_cidr | IPv4 CIDR of k8s cluster used for ES communication. | `any` | n/a | yes |
| cluster\_name | ES cluster name. | `string` | n/a | yes |
| data\_disk\_size | Persistent disk size specified in GB. | `any` | n/a | yes |
| data\_disk\_type | Type of disk used as a persistent storage. | `string` | `"pd-ssd"` | no |
| heap\_size | Heap size setting for ES. | `string` | `"1800m"` | no |
| instance\_name | Base for GCE instances name. | `any` | n/a | yes |
| k8s\_enable | Enable k8s extension to deploy endpoints to cluster members and internal load balancer as a k8s service, use only with k8s provider setup previously | `bool` | `false` | no |
| namespace | K8s namespace used to deploy endpoints and services. | `string` | `"production"` | no |
| node\_count | Number of ES nodes to deploy. | `string` | `"1"` | no |
| project | Name of GCP project. | `string` | n/a | yes |
| raw\_image\_source | URL of tar archive containing RAW source for ES image (you can use Packer image template to generate image, as mentioned above). | `string` | `"https://storage.googleapis.com/ackee-images/ackee-elasticsearch-7-disk-79.tar.gz"` | no |
| region | Region of GCP project. | `string` | n/a | yes |
| zone | Zone of GCP project - optional parameter, if not set, the instances will be spread across the available zones. | `any` | `null` | no |

## Outputs

No output.

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
