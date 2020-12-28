<hidden>
---

copyright:
  years: 2017, [{CURRENT_YEAR}]
lastupdated: "[{LAST_UPDATED_DATE}]"

keywords: install Terraform on {{site.data.keyword.cloud_notm}} cli, set up {[provider]} cli, ibm cloud provider plugin, ibm cloud for {[provider]}

subcollection: terraform

---
{[headtag.md]}

# Setting up the {[provider]} CLI and the {{site.data.keyword.cloud_notm}} Provider plug-in
{: #tf-provider}

Before you can automate your {{site.data.keyword.cloud_notm}} resource provisioning, you must install the {[provider]} CLI and the {{site.data.keyword.cloud_notm}} Provider plug-in. 
{: shortdesc}

## Version information 
{: #versions}

The resources and data sources in this documentation are based on the following versions:

- **IBM Cloud Provider plug-in for {[provider]} version**: 1.9.0
- **{[provider]} version**: 0.12

With the release of {[provider]} version 0.12, the syntax for configuration files changed. If you want to run your infrastructure code by using {[provider]} version 0.12, you must first [update your configuration files](#tf-0.1x-migration) to apply the new syntax. 
{: important}

{[cli-install.md]}
</hidden>
