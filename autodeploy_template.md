---

copyright:
  years: 2017, [{CURRENT_YEAR}]
lastupdated: "[{LAST_UPDATED_DATE}]"

keywords: terraform provider deployment, automation, schematics workspace, ibm cloud terraform provider deployment, schematics workspace creation, auto deploy 

subcollection: terraform

---

{[headtag.md]}

# Creating a deployment to IBM Cloud Schematics link
{: #create_deploy_to_schematics}

The deployment to {{site.data.keyword.cloud_notm}} link is an efficient way to share your public Git repository so that other people can to create workspace by using Schematics without affecting your original code. The link requires minimal configuration and you can insert it anywhere that supports markup. If you click the hyper link, the configuration for the Schematic workspace is setup and you need to only click create button for workspace creation in Schematics.
{: shortdesc}

The following steps help to create a deployment to {[provider]} v0.12 provider template example in {{site.data.keyword.bplong_notm}}.

1. Create a template example by using {[provider]} provider and publish in the public Git repository. To create example, refer [Sample template example](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples){: external}.
2. Copy the public Git repository URL, for example, `https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-api-gateway`.
3. Use this syntax to auto deploy the Schematics workspace creation in the {{site.data.keyword.cloud_notm}}.

  **Syntax**

  ```
  https://cloud.ibm.com/schematics/workspaces/create?repository=<template public Git repository example url>&terraform_version=<terraform_v0.xx>
  ```
  {: pre}

  **Example**

  ```
  https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-api-gateway&terraform_version=terraform_v0.12
  ```
  {: pre}

  The URL contains two parameters, first parameter is provided with the workspace name as `ibm-api-gateway` and second parameter is provided with the {[provider]} version as `terraform_v0.12`. For more information, about the parameters refer to this example, `https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/<ibm-api-gateway>.&<terraform_version=terraform_v0.12>`. If you do not provide any parameters of ignore one parameter, the `Deploy to {{site.data.keyword.cloud_notm}}` link defaults to the repository's master branch. You can provide the {[provider]} version parameter that you are using.
  {: important}

4. You can copy, and paste the example URL in the browser to view the {{site.data.keyword.cloud_notm}} Schematics workspace UI with the create button is display.
5. Cross-check the parameters in the workspace UI and click `Create` button.

## Adding an image on deployment to {{site.data.keyword.cloud_notm}} hyperlink
{: #add_an_image}

You can add an image on `Deploy to {{site.data.keyword.cloud_notm}} Schematics` text by using the following syntax and example.

**Syntax**
```
<a href="https://cloud.ibm.com/schematics/workspaces/create?repository=<public Git repository example URL>/<workspace name>&terraform_version=terraform_xx">Deploy to {{site.data.keyword.bplong_notm}} <img src=<image location>></a>
```
{: pre}

**Example**

```
<a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-api-gateway&terraform_version=terraform_v0.12">Deploy to {{site.data.keyword.cloud_notm}}<img src="/images/deploytoschematics.png"></a>
```
{: pre}

**Output**

<img src="/images/deploytoschematics.png" alt="Deploy to {{site.data.keyword.cloud_notm}}" width="200" style="width: 200px; border-style: none"/>

To view about the sample {[provider]} template examples, refer [Sample {[provider]} templates and deploy to {{site.data.keyword.bplong_notm}}](/docs/terraform?topic=terraform-sample_terraformtemplates#api-gwy-template).

