# Azure Cloud Governance & Cost Automation

## Executive summary

Azure environments can accumulate resources with missing ownership, inconsistent settings and unnecessary costs. This project will use Terraform, Azure Policy, Azure Resource Graph and PowerShell to identify selected issues, enforce configuration rules and verify approved corrections. GitHub Actions will run the automation, and an Azure Workbook will present the findings.

**Status:** Planning and design. Implementation and Azure validation have not started.

## Planned scope

- Inventory resources within dedicated resource groups.
- Check ownership tags, selected network and storage settings, and unattached resources that need review.
- Generate findings before making changes, then verify approved corrections.
- Manage policy assignments, identities, permissions and reporting through Terraform.
- Run workflows through GitHub Actions using OpenID Connect authentication.

## Verification plan

Deploy the project in Azure and record the expected audit findings, policy enforcement, before-and-after corrections and repeat audit results. Capture the workflow logs and dashboard, then remove the deployed resources and verify cleanup.

Cost recommendations will be separated from measured savings. An unattached resource will be treated as a review candidate, not automatic permission to delete it.
