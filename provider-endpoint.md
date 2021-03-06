---

copyright:
  years: 2017, [{CURRENT_YEAR}]
lastupdated: "[{LAST_UPDATED_DATE}]"

keywords: terraform provider, terraform provider private endpoint, private endpoint

subcollection: terraform

---

{[headtag.md]}

# Configure the {[provider]} provider to use the private service endpoint
{: #config-provider}

The steps involved in configuring your {[provider]} runtime to use the private Cloud Service Endpoint (CSE) of an {{site.data.keyword.cloud_notm}} service within <staging> [Stage environment](https://test.cloud.ibm.com) or</staging> public CSE in [Production environment](https://cloud.ibm.com).

You can configure the {{site.data.keyword.cloud_notm}} provider for {[provider]} to communicate with an {{site.data.keyword.cloud_notm}} service by using the service's private service endpoint.
{: shortdesc}

1. Setup the {[provider]} engine and an {{site.data.keyword.cloud_notm}} provider, in {{site.data.keyword.cloud_notm}} virtual machine by using private VLAN. And provision the enabled Virtual Routing and Forwarding (VRF) account. For information about the {{site.data.keyword.bplong_notm}} private end points, see [{{site.data.keyword.bplong_notm}} endpoint prerequisites](/docs/schematics?topic=schematics-private-endpoints#private-network-prereqs).
2. Export the following environment variables on your local machine. For more information, about supported private service endpoints for each {{site.data.keyword.cloud_notm}} service to support in production, see [Use service endpoints](/docs/account?topic=account-vrf-service-endpoint).
3. Initialize the {[provider]} CLI to load the environment variables that you set.

```
terraform init
```
{: pre}

|Service|Environment variable key|Private service endpoint|
|-------------|--------|----------------|
|Account management|`IBMCLOUD_ACCOUNT_MANAGEMENT_API_ENDPOINT`|N/A|
|Certificate manager|`IBMCLOUD_CERTIFICATE_MANAGER_API_ENDPOINT`|N/A|
|Cloud Foundry|`IBMCLOUD_MCCP_API_ENDPOINT`|N/A|
|Cloud functions|`IBMCLOUD_NAMESPACE_API_ENDPOINT`|N/A|
|Containers|`IBMCLOUD_CS_API_ENDPOINT`|[Docs](/docs/containers?topic=containers-plan_clusters#workeruser-master)|
|CIS|`IBMCLOUD_CIS_API_ENDPOINT`|N/A|
|Direct Link|`IBMCLOUD_DL_API_ENDPOINT`|N/A|
|GHoST / Tagging|`IBMCLOUD_GT_API_ENDPOINT`|N/A|
|HPCS|`IBMCLOUD_HPCS_API_ENDPOINT`|N/A|
|IAM|`IBMCLOUD_IAM_API_ENDPOINT`|N/A|
|IAMPAP|`IBMCLOUD_IAMPAP_API_ENDPOINT`|N/A|
|ICD|`IBMCLOUD_ICD_API_ENDPOINT`|[Docs](/docs/account?topic=account-vrf-service-endpoint)|
|Key protect|`IBMCLOUD_KP_API_ENDPOINT`|`https://private.<region>.kms.cloud.ibm.com`|
|Private DNS|`IBMCLOUD_PRIVATE_DNS_API_ENDPOINT`| N/A|
|Resource management|`IBMCLOUD_RESOURCE_MANAGEMENT_API_ENDPOINT`|N/A|
|Resource controller|`IBMCLOUD_RESOURCE_CONTROLLER_API_ENDPOINT`|N/A|
|Resource catalog|`IBMCLOUD_RESOURCE_CATALOG_API_ENDPOINT`|N/A|
|Schematics|`IBMCLOUD_SCHEMATICS_API_ENDPOINT`|`https://private-us.schematics.cloud.ibm.com` <br> `https://private-eu.schematics.cloud.ibm.com`|
|Transit Gateway|`IBMCLOUD_TG_API_ENDPOINT`| N/A|
|UAA|`IBMCLOUD_UAA_ENDPOINT`|N/A|
|User management|`IBMCLOUD_USER_MANAGEMENT_ENDPOINT`|N/A|
|VPC Gen2|`IBMCLOUD_IS_NG_API_ENDPOINT`|N/A|

