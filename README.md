# Terraform AWS EKS Module

Terraform configuration to create an AWS EKS cluster

Adapted from https://github.com/terraform-providers/terraform-provider-aws

For details, see https://www.terraform.io/docs/providers/aws/guides/eks-getting-started.html

Configures an AWS account with the following resources:

* EKS Kubernetes API server
* VPC with:
  * "10.0.0.0/16" CIDR block
  * 2 subnets, each in a different availability zone with:
    * "10.0.x.0/24" CIDR block
  * Internet gateway
* EC2 autoscaling group for worker nodes, with:
  * 1-2 m4.large instances
  * 2 subnets
