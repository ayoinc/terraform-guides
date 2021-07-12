# Terraform Guides

[![IaC](https://app.soluble.cloud/api/v1/public/badges/d53bf517-41f3-4a00-b766-698ad8f3492a.svg)](https://app.soluble.cloud/repos/details/github.com/ayoinc/terraform-guides)  [![CIS](https://app.soluble.cloud/api/v1/public/badges/953e00af-04cd-4e90-9c10-9a16400022f4.svg)](https://app.soluble.cloud/repos/details/github.com/ayoinc/terraform-guides)  [![HIPAA](https://app.soluble.cloud/api/v1/public/badges/d7caa9e4-7c6a-486f-a529-d4fd90fafde8.svg)](https://app.soluble.cloud/repos/details/github.com/ayoinc/terraform-guides)  
This repository contains sample Terraform configurations, Sentinel policies, and automation scripts that can be used with Terraform Enterprise.

## infrastructure-as-code
This directory contains sample Terraform configurations to provision VMs into AWS, Azure, and Google Cloud Platform (GCP) as well as Kubernetes clusters into Azure Container Service (ACS) and Google Kubernetes Engine (GKE).

## self-serve-infrastructure
This directory contains sample Terraform configurations to enable self-service infrastructure. In particular, it illustrates how developers can deploy applications to Kubernetes clusters provisioned by an operations team.

## governance
This directory contains some sample Sentinel policies for several clouds which ensure that all infrastructure provisioned with Terraform Enterprise complies with an organization's provisioning rules.

## operations
This directory provides artifacts that can be used by operations teams using Terraform Enterprise. In particular, it includes scripts that show how the Terraform Enterprise REST API can be used to automate interactions with Terraform Enterprise, set and delete variables in workspaces, and export, import, and delete Sentinel policies.

## cloud-management-platform
This directory provides samples of how Terraform can be used to support cloud management platforms.

## `gitignore.tf` Files

You may notice some [`gitignore.tf`](operations/provision-consul/best-practices/terraform-aws/gitignore.tf) files in certain directories. `.tf` files that contain the word "gitignore" are ignored by git in the [`.gitignore`](./.gitignore) file.

If you have local Terraform configuration that you want ignored (like Terraform backend configuration), create a new file in the directory (separate from `gitignore.tf`) that contains the word "gitignore" (e.g. `backend.gitignore.tf`) and it won't be picked up as a change.
