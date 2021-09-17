# Exam AZ-500

- [Manage Identity and Access](#Manage-Identity-and-Access)
- [Implement Platform Protection](#Implement-Platform-Protection)
- [Manage Security Operations](#Manage-Security-Operations)
- [Secure Data and Applications](#Secure-Data-and-Applications)

## Manage Identity and Access

### Manage Azure Active Directory (Azure AD) Identities

1. Create and manage a managed identity for Azure resources

1. Manage Azure AD groups

    * A group is a collection of users. Types of groups include:
        * Security Group
        * Office 365 Group

    * Membership types for security groups include:
        * **Assigned:** The administrator adds or remove members.
        * **Dynamic User:** Membership determined based on attribute values. Queries determine which attributes are used to determine group membership.
        * Dynamic Device (security groups only)

    * Security groups can be nested. However, there are some restrictions on nested groups. You cannot:
        * Add groups to groups synced with on-premises Active Directory.
        * Add security groups to Office 365 groups.
        * Add Office 365 groups to other Office 365 groups or to security groups.
        * Assign apps to nested groups.
        * Apply licenses to nested groups.

    * Groups can be managed via:
        * Azure Portal
        * Azure PowerShell
        * Azure CLI

    * To create a group in PowerShell:
        ```PowerShell
        New-AzADGroup -DisplayName "Sales" -MailNickname "Sales"
        ```

    * To create a group using the CLI:
        ```bash
        az ad group create --display-name "Marketing" --mail-nickname "Marketing"
        ```

1. Manage Azure AD users

    * A user is an account required to access Azure resources. This includes Software as a Service (SaaS) applications such as Office 365, as well as custom applications written by your in-house development team.

    * A user can be one of:
        * Cloud based user account (Azure Active Directory)
        * A synchronised on-premises directory account
        * A guest user

    * Users can be managed via:
        * Azure Portal
        * Azure PowerShell
        * Azure CLI

    * To create a user in PowerShell:
        ```PowerShell
        $SecureStringPassword = ConvertTo-SecureString -String "Password.1" -AsPlainText -Force
        New-AzADUser -DisplayName "Test User2" -UserPrincipalName "testuser2@sjohnsontexansfans.onmicrosoft.com" -Password $SecureStringPassword -MailNickname testuser2
        ```

    * To create a user using the CLI:
        ```bash
        az ad user create --display-name "Test User3" --password "Password.1" --user-principal-name testuser3@sjohnsonexansfans.onmicrosoft.com
        ```


1. Manage external identities by using Azure AD

1. Manage administrative units

### Manage Secure Access by Using Azure AD

1. Configure Azure AD Privileged Identity Management (PIM)

1. Implement Conditional Access policies, including multifactor authentication

1. Implement Azure AD Identity Protection

1. Implement passwordless authentication

1. Configure access reviews

### Manage Application Access

1. Integration single sign-on (SSO) and identity providers for authentication

1. Create an app registration

1. Configure app registration permission scopes

1. Manage app registration permission consent

1. Manage API permissions to Azure subscriptions and resources

1. Configure an authentication method for a service principal

### Manage Access Control

1. Configure Azure role permissions for management groups, subscriptions, resource groups, and resources

1. Interpret role and resource permissions

1. Assign built-in Azure AD roles

1. Create and assign custom roles, including Azure roles and Azure AD roles

## Implement Platform Protection

### Implement Advanced Network Security

1. Secure the connectivity of hybrid networks

1. Secure the connectivity of virtual networks

1. Create and configure Azure Firewall

1. Create and configure Azure Firewall Manager

1. Create and configure Azure Application Gateway

1. Create and configure Azure Front Door

1. Create and configure Web Application Firewall (WAF)

1. Create a resource firewall, including storage account, Azure SQL, Azure Key Vault, or Azure App Service

1. Configure network isolation for Web Apps and Azure Functions

1. Implement Azure Service Endpoints

1. Implement Azure Private Endpoints, including integrating with other services

1. Implement Azure Private Links

1. Implement Azure DDoS Protection

### Configure Advanced Security for Compute

1. Configure Azure Endpoint Protection for virtual machines (VMs)

1. Implement and manage security updates for VMs

1. Configure security for container services

1. Manage access to Azure Container Registry

1. Configure security for serverless compute

1. Configure security for an Azure App Service

1. Configure encryption at rest

1. Configure encryption in transit

## Manage Security Operations

### Configure Centralised Policy Management

1. Configure a custom security policy

1. Create a policy initiative

1. Configure security settings and auditing by using Azure Policy

### Configure and Manage Threat Protection

1. Configure Azure Defender for servers (not including Microsoft Defender for Endpoint)

1. Evaluate vulnerability scans from Azure Defender

1. Configure Azure Defender for SQL

1. Use the Microsoft Threat Modelling Tool

### Configure and Manage Security Monitoring Solutions

1. Create and customise alert rules by using Azure Monitor

1. Configure diagnostic logging and log retention by using Azure Monitor

1. Monitor security logs by using Azure Monitor

1. Create and customise alert rules in Azure Sentinel

1. Configure connections in Azure Sentinel

1. Evaluate alerts and incidents in Azure Sentinel

## Secure Data and Applications

### Configure Security for Storage

1. Configure access control for storage accounts

1. Configure storage account access keys

1. Configure Azure AD authentication for Azure Storage and Azure Files

1. Configure delegated access

### Configure Security for Data

1. Enable database authentication by using Azure AD

1. Enable database auditing

1. Configure dynamic masking on SQL workloads

1. Implement database encryption for Azure SQL Database

1. Implement network isolation for data solutions, including Azure Synapse Analytics and Azure Cosmos DB

### Configure and Manage Azure Key Vault

1. Create and configure Key Vault

1. Configure access to Key Vault

1. Manage certificates, secrets, and keys

1. Configure key rotation

1. Configure backup and recovery of certificates, secrets, and keys
