---

copyright:
  years: 2017, [{CURRENT_YEAR}]
lastupdated: "[{LAST_UPDATED_DATE}]"

keywords: terraform templates, schematics template

subcollection: terraform

---


{[headtag.md]}


# Sample {[provider]} templates and deploy to {{site.data.keyword.cloud_notm}}
{: #sample_terraformtemplates}

All {[provider]} templates use the {[provider]} version 0.12 format.
{: note}

The sample {[provider]} templates and deploy to {{site.data.keyword.cloud_notm}} link is an efficient way to access the templates and experience the auto deploy to the {{site.data.keyword.cloud_notm}} to create workspace in Schematics.
{: shortdesc}

When you click the `Deploy to {{site.data.keyword.cloud_notm}}` following actions occur:

  1. If the user does not have an active {{site.data.keyword.cloud_notm}} account, you must create a trial account or a real account.

  2. The user can select a region, resource group (available in the Dallas, Washington, London, Frankfurt, and Tokyo regions) or organization and space (available in the Dallas, London, and Frankfurt regions).

  3. The auto deploy link creates a workspace in the {{site.data.keyword.bplong_notm}}.

  4. To execute `generate plan` successfully, you need to configure the required variables.

<publish>

## API Gateway templates
{: #api-gwy-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
    <tr>
      <td><code>ibm-api-gateway</code></td>
      <td>Create an [IBM Cloud API Gateway](/docs/api-gateway?topic=api-gateway-whatis_apigw) service instance to set up an API for an IBM Cloud service of your choice. You can specify the API endpoint that you want to use to access your service, and define subscription keys so that developers can securely consume your API.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_api_gateway_endpoint</code></li><li style="margin:0px; padding:0px"><code>ibm_api_gateway</code></li><li style="margin:0px; padding:0px"><code>ibm_api_gateway_endpoint_subscription</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-api-gateway"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-api-gateway&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
 </tr>
  </tbody>
  </table>
 
## Certificate Manager templates
{: #cert-mgr-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
 <tr>
   <td><code>ibm-certificate-manager-order</code></td>
      <td> Create an IBM Cloud Internet Services instance with a domain, and use [IBM Cloud Certificate Manager](/docs/certificate-manager?topic=certificate-manager-about-certificate-manager) to generate a TLS certificate for this domain.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_cis</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_domain</code></li><li style="margin:0px; padding:0px"><code>ibm_certificate_manager_order</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-certificate-manager/ibm-certificate-manager-order"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-certificate-manager/ibm-certificate-manager-order&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
	  </tr>
	</tbody>
	</table>

## Cloud Foundry templates
{: #cloud-foundry-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
    <tr>
      <td><code>ibm-app</code></td>
      <td>Create and deploy a Cloud Foundry app in {{site.data.keyword.cloud_notm}}.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>null_resource</code></li><li style="margin:0px; padding:0px"><code>ibm_app_route</code></li><li style="margin:0px; padding:0px"><code>ibm_service_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_service_key</code></li><li style="margin:0px; padding:0px"><code>ibm_app</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-app"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-app&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
    </tr>
</tbody>
</table>


## Direct Link templates
{: #dl-template}

   <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-dl-gateway</code></td>
      <td>Create a speed and reliable direct link gateways, virtual connections, offering information, routers, and ports by using the resources.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_dl_gateway</code></li><li style="margin:0px; padding:0px"><code>ibm_dl_virtual_connection</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-direct-link"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-direct-link&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  </tbody>
  </table>

## Event Streams templates
{: #event-stream-template}

   <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-event-streams</code></td>
      <td>Create a communication through an event streams instance, topic instance, or Kafka consumer application to connect an existing event stream instances and its topic instance by using {{site.data.keyword.bplong_notm}} workspace.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_event_streams_topic</code></li><li style="margin:0px; padding:0px"><code>kafka_consumer_app</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-event-streams"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-event-streams&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  </tbody>
  </table>


## Functions templates
{: #func-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
     <tr>
    <td><code>ibm-function-cloudant-trigger</code></td>
	<td>Create a Cloudant NoSQL service instance and a Python app deployment that creates the `database demo` database in your service instance. Then, you create an action with {{site.data.keyword.cloud_notm}} functions that is triggered when you add or edit documents to your database.<br><br>**Resources**<br>
	  <ul style="margin:0px 0px 0px 20px; padding:0px">
	  <li style="margin:0px; padding:0px"><code>null_resource</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_service_instance</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_service_key</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_app_route</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_app</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_function_package</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_function_action</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_function_trigger</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_function_rule</code></li>
	  </ul></td>
    <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-function-cloudant-trigger"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-function-cloudant-trigger&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
   </tbody>
  </table>

## Identity & Access (IAM) templates
{: #iam-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-iam-custom-role</code></td>
      <td>Create a custom role in IBM Cloud Identity and Access Management (IAM) for IBM Cloud Key Protect.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_iam_custom_role</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iam-custom-role"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iam-custom-role&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  <tr>
    <td><code>ibm-iam-policy</code></td>
      <td>Create an access policy in IBM Cloud Identity and Access Management (IAM) to grant permissions for a resource group to a user.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_iam_user_policy</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iam-policy"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iam-policy&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  </tbody>
  </table>

## Key Management Service templates
{: #kms-template}

   <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-key-management-service</code></td>
      <td>Create an {{site.data.keyword.cos_full_notm}} service instance with a bucket to store your data and provide a key management service resource for Hyper Protect Crypto Services and Key Protect service instance with a root key. This allow access between these services with an IBM Cloud Identity and Access Management policy.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_kms_key</code></li><li style="margin:0px; padding:0px"><code>ibm_kp_key</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-kms"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-kms&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  <tr>
    <td><code>ibm-hpcs-crypto</code></td>
      <td>Create an {{site.data.keyword.cos_full_notm}} service instance with a bucket to store your data and provide a key management service resource for Hyper Protect Crypto Services instance with a root key. This allow access between these services with an IBM Cloud Identity and Access Management policy.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_kms_key</code></li><li style="margin:0px; padding:0px"><code>ibm_kp_key</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-hpcs-crypto"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-hpcs-crypto&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  </tbody>
  </table>

## Kubernetes templates
{: #kubernetes-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
 <tr>
   <td><code>vpc-classic-cluster</code></td>
      <td>Create an {{site.data.keyword.containerfull_notm}} cluster in a Virtual Private Cloud (VPC) for Generation 1 compute with worker nodes in a default worker pool that you spread across two zones. You can provision an IBM Cloud Object Storage service, and bind this service to the cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><listyle="margin:0px; padding:0px"><code>ibm_is_vpc</code></li><li style="margin:0px; padding:0px"><code>ibm_is_subnet</code></li><li style="margin:0px; padding:0px"><code>ibm_container_vpc_cluster</code></li><li style="margin:0px; padding:0px"><code>ibm_container_vpc_worker_pool</code></li><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_container_bind_service</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-cluster/vpc-classic-cluster"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-cluster/vpc-classic-cluster&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  <tr>
   <td><code>vpc-gen2-cluster</code></td>
      <td>Create an {{site.data.keyword.containerfull_notm}} cluster in a Virtual Private Cloud (VPC) for Generation 2 compute with worker nodes in a default worker pool that you spread across two zones. Also, you provision an IBM Cloud Object Storage service, and bind this service to the cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li><li style="margin:0px; padding:0px"><code>ibm_is_subnet</code></li><li style="margin:0px; padding:0px"><code>ibm_container_vpc_cluster</code></li><li style="margin:0px; padding:0px"><code>ibm_container_vpc_worker_pool</code></li><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_container_bind_service</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-cluster/vpc-gen2-cluster"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-cluster/vpc-gen2-cluster&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
   <tr>
    <td><code>ibm-iks-classic-ROKS</code></td>
      <td>Create a Red Hat View GitHub repository on IBM Cloud cluster that runs version 3.11 of the View GitHub repository Container Platform.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iks-classic-ROKS"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iks-classic-ROKS&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  </tbody>
  </table>


## Transit Gateway templates
{: #transit-gwy-template}

   <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-transit-gateway</code></td>
      <td>Create a transit gateways, list available connections, and locations for the gateways.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_tg_gateway</code></li><li style="margin:0px; padding:0px"><code>ibm_tg_connection</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-transit-gateway"><img src="/images/viewgithub.png"></a><br><br><a href="https://cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-transit-gateway&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>

  </tr>
  </tbody>
  </table>

</publish>

<staging>

## API Gateway templates
{: #api-gwy-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
    <tr>
      <td><code>ibm-api-gateway</code></td>
      <td>Create an [IBM Cloud API Gateway](/docs/api-gateway?topic=api-gateway-whatis_apigw) service instance to set up an API for an IBM Cloud service of your choice. You can specify the API endpoint that you want to use to access your service, and define subscription keys so that developers can securely consume your API.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_api_gateway_endpoint</code></li><li style="margin:0px; padding:0px"><code>ibm_api_gateway</code></li><li style="margin:0px; padding:0px"><code>ibm_api_gateway_endpoint_subscription</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-api-gateway"><img src="/images/viewgithub.png"></a><br><br><a href="https://test.cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-api-gateway&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
    </tr>
  </tbody>
  </table>
 
## Certificate Manager templates
{: #cert-mgr-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
 <tr>
   <td><code>ibm-certificate-manager-order</code></td>
      <td> Create an IBM Cloud Internet Services instance with a domain, and use [IBM Cloud Certificate Manager](/docs/certificate-manager?topic=certificate-manager-about-certificate-manager) to generate a TLS certificate for this domain.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_cis</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_domain</code></li><li style="margin:0px; padding:0px"><code>ibm_certificate_manager_order</code></li></ul></td>
     <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-certificate-manager/ibm-certificate-manager-order"><img src="/images/viewgithub.png"></a><br><br><a href="https://test.cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-certificate-manager/ibm-certificate-manager-order&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
	  </tr>
	</tbody>
	</table>

## Classic Infrastructure templates
{: #classic-infra-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
   <td><code>ibm-bulk-vsi</code></td>
      <td> Create a classic [IBM Cloud Virtual Server](/docs/virtual-servers?topic=virtual-servers-about-virtual-servers) instance with multiple hostnames.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li></ul></td>
	  <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-bulk-vsi) <br></td>
  </tr>
  <tr>
   <td><code>ibm-compute-public-ip</code></td>
      <td>Create a classic virtual server instance with custom firewall settings, and run a script to install a web server and Nginx on your instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_network_public_ip</code></li><li style="margin:0px; padding:0px"><code>ibm_firewall</code></li><li style="margin:0px; padding:0px"><code>ibm_firewall_policy</code></li></ul></td>
	  <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-compute-public-ip) <br></td>
  </tr>
  <tr>
    <td><code>ibm-lb-vpx</code></td>
      <td>Create a classic virtual server instance that you can access by using an SSH key and a {{site.data.keyword.vpx_full}} load balancer that is exposed with a virtual IP address.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_lb_vpx_vip</code></li><li style="margin:0px; padding:0px"><code>ibm_lb_vpx_service</code></li></ul></td>
	  <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-lb-vpx) <br></td>
  </tr>
   <tr>
    <td><code>ibm-lbaas</code></td>
      <td>Create an {{site.data.keyword.Bluemix_notm}} {{site.data.keyword.loadbalancer_short}} for a classic virtual server instance. You configure the load balancer to manage incoming HTTPS and HTTP network traffic and set up health monitoring for your virtual server instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_ssl_certificate</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_lbaas</code></li></li><li style="margin:0px; padding:0px"><code>ibm_lbaas_server_instance_attachment</code></li><li style="margin:0px; padding:0px"><code>ibm_lbaas_health_monitor</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-lbaas) <br></td>
  </tr>
  <tr>
    <td><code>ibm-network-vlan</code></td>
      <td>Create a classic virtual server instance with a public and a private VLAN that you can access by using an SSH key.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_network_vlan</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li></ul></td>
	<td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-network-vlan)<br></td>
  </tr>
  <tr>
    <td><code>ibm-vsi-cloudinit</code></td>
      <td>Create a classic virtual server instance that is configured with an SSH key and connected to a public and private VLAN, and use CloudInit to install an Apache (HTTPD) web server on the instance. Your SSH key is used to create a VPN connection to your virtual server instance to start the Apache web server.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_network_vlan</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li>
    </ul></td>
	<td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-vsi-cloudinit) <br></td>
  </tr>
  <tr>
    <td><code>ibm-vsi-fault-tolerance</code></td>
      <td>Create an IBM VSI virtual machine by using an {{site.data.keyword.CloudDataCents_notm}} choice. To use the template, you must provide a classic infrastructure user name and API key, as well as an {{site.data.keyword.cloud_notm}} API key. For more information, about how to retrieve these values, see [Supported input parameters](/docs/terraform?topic=terraform-provider-reference#provider-parameter-ov). If the virtual server instance cannot be created in the first data center, {{site.data.keyword.cloud_notm}} tries to create the instance in the subsequent data center until the order can be completed.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li></ul></td>
	<td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-vsi-fault-tolerance) <br></td>
  </tr>
<tr>
    <td><code>ibm-vsi-placement-group</code></td>
      <td>Create a classic virtual server instance with a placement group.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_placement_group</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li></ul</td>
	      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-vsi-placement-group)</td>
  </tr>
 <tr>
    <td><code>ibm-vsi</code></td>
      <td>Create a classic virtual server instance with a private VLAN only.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li></ul></td>
	 <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-vsi)</td>
  </tr>
  <tr>
    <td><code>ibm-website-multi-region</code></td>
	  <td>Provision a highly available website architecture across multiple regions on {{site.data.keyword.cloud_notm}} classic infrastructure with {[provider]}. Then, deploy a single instance of Wordpress by using Ansible, and replicate Wordpress across the two regions to explore the security and resiliency features of IBM Cloud Security Groups, DNS, Web Application Firewall (WAF), and global and local load balancers. For more information, about how to use this template, see [Tutorial: Deploying Wordpress in a highly available, cross-region website architecture with {[provider]} and Ansible](/docs/terraform?topic=terraform-multi_region).<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_lbaas</code></li><li style="margin:0px; padding:0px"><code>ibm_lbaas_server_instance_attachment</code></li><li style="margin:0px; padding:0px"><code>ibm_lbaas_health_monitor</code></li></ul></td>
	  <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-website-multi-region)</td>
  </tr>
  <hidden><tr>
    <td><code>ibm-website-single-region</code></td>
      <td>Provision a single-site website architecture on {{site.data.keyword.cloud_notm}} classic infrastructure with {[provider]}. Then, use Ansible to deploy multiple Apache web servers with a single MariaDB database host on your {{site.data.keyword.cloud_notm}} classic virtual servers. The private IP addresses of the Apache web servers are added to the {{site.data.keyword.cloud_notm}} Load Balancer that serves as the public endpoint for your Wordpress deployment. For more information, about how to use the template, see Tutorial [Deploying Wordpress on IBM Cloud classic infrastructure with {[provider]} and Ansible](/docs/terraform?topic=terraform-deploy_wordpress).<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_lbaas</code></li><li style="margin:0px; padding:0px"><code>ibm_lbaas_server_instance_attachment</code></li><li style="margin:0px; padding:0px"><code>ibm_lbaas_health_monitor</code></li></ul></td>
	  <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-website-single-region)</td>
  </tr></hidden>
  </tbody>
  </table>

## Cloud Databases templates
{: #cloud-db-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
     <td><code>ibm-database</code></td>
      <td>Create a classic virtual server instance and an {{site.data.keyword.cloud_notm}} database for PostgreSQL instance, and set up connectivity between the instances.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_resource_group</code></li><li style="margin:0px; padding:0px"><code>ibm_database</code></li></ul</td>
	      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-database)</td>
  </tr>
     </tbody>
  </table>

## Cloud Foundry templates
{: #cloud-foundry-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
    <tr>
      <td><code>ibm-app</code></td>
      <td>Create and deploy a Cloud Foundry app in {{site.data.keyword.cloud_notm}}.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>null_resource</code></li><li style="margin:0px; padding:0px"><code>ibm_app_route</code></li><li style="margin:0px; padding:0px"><code>ibm_service_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_service_key</code></li><li style="margin:0px; padding:0px"><code>ibm_app</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-app"><img src="/images/viewgithub.png"></a><br><br><a href="https://test.cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-app&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
    </tr>
</tbody>
</table>

## Direct Link templates
{: #dl-template}

   <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-dl-gateway</code></td>
      <td>Create a speed and reliable direct link gateways, virtual connections, offering information, routers, and ports by using the resources.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_dl_gateway</code></li><li style="margin:0px; padding:0px"><code>ibm_dl_virtual_connection</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-direct-link"><img src="/images/viewgithub.png"></a><br><br><a href="https://test.cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-direct-link&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  </tbody>
  </table>

## DNS templates
{: #dns-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
 <tr>
    <td><code>ibm-private-dns</code></td>
      <td>Create an {{site.data.keyword.vpc_short}} and an {{site.data.keyword.dns_full_notm}} instance, and add the VPC as a permitted network to the DNS service instance. Then, you create different types of DNS records.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_dns_zone</code></li><li style="margin:0px; padding:0px"><code>ibm_dns_resource_record</code></li></ul></td>
	 <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-private-dns)</td>
  </tr>
  </tbody>
  </table>
  
## Event Streams templates
{: #event-stream-template}

   <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-event-streams</code></td>
      <td>Create a communication through an event streams instance, topic instance, or Kafka consumer application to connect an existing event stream instances and its topic instance by using {{site.data.keyword.bplong_notm}} workspace.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_event_streams_topic</code></li><li style="margin:0px; padding:0px"><code>kafka_consumer_app</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-event-streams"><img src="/images/viewgithub.png"></a><br><br><a href="https://test.cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-event-streams&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  </tbody>
  </table>

## Functions templates
{: #func-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
     <tr>
    <td><code>ibm-function-cloudant-trigger</code></td>
	<td>Create a Cloudant NoSQL service instance and a Python app deployment that creates the `database demo` database in your service instance. Then, you create an action with {{site.data.keyword.cloud_notm}} functions that is triggered when you add or edit documents to your database.<br><br>**Resources**<br>
	  <ul style="margin:0px 0px 0px 20px; padding:0px">
	  <li style="margin:0px; padding:0px"><code>null_resource</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_service_instance</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_service_key</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_app_route</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_app</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_function_package</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_function_action</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_function_trigger</code></li>
	  <li style="margin:0px; padding:0px"><code>ibm_function_rule</code></li>
	  </ul></td>
    <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-function-cloudant-trigger"><img src="/images/viewgithub.png"></a><br><br><a href="https://test.cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-function-cloudant-trigger&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
   </tbody>
  </table>


## Identity & Access (IAM) templates
{: #iam-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-iam-custom-role</code></td>
      <td>Create a custom role in IBM Cloud Identity and Access Management (IAM) for IBM Cloud Key Protect.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_iam_custom_role</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iam-custom-role"><img src="/images/viewgithub.png"></a><br><br><a href="https://test.cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iam-custom-role&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  <tr>
    <td><code>ibm-iam-policy</code></td>
      <td>Create an access policy in IBM Cloud Identity and Access Management (IAM) to grant permissions for a resource group to a user.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_iam_user_policy</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iam-policy"><img src="/images/viewgithub.png"></a><br><br><a href="https://test.cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iam-policy&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  <tr>
    <td><code>ibm-iam-user-invite</code></td>
      <td>Create an access group in {{site.data.keyword.IBM_notm}} {{site.data.keyword.iamshort}} and assign this access group permission to a resource group. Then, you add users to your access group and assign these users access to IBM Cloud Kubernetes Service, classic IBM Cloud infrastructure, and Cloud Foundry.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_iam_access_group</code></li><li style="margin:0px; padding:0px"><code>ibm_iam_access_group_policy</code></li><li style="margin:0px; padding:0px"><code>ibm_iam_user_invite</code></li></ul</td>
	      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iam-user-invite)</td>
  </tr>
  </tbody>
  </table>


## Internet templates 
{: #internet-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
   <td><code>ibm-cis</code></td>
      <td> Create an IBM Cloud Internet Service instance and configure the instance with health check monitoring, origin pool, global load-balancing, DNS records, firewall, and limit the rate rules.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_cis</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_domain_settings</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_domain</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_edge_functions_action</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_edge_functions_trigger</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_healthcheck</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_origin_pool</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_global_load_balancer</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_dns_record</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_firewall</code></li><li style="margin:0px; padding:0px"><code>ibm_cis_rate_limit</code></li></ul></td>
	  <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-cis)</td>
  </tr>
</tbody>
</table>

## Key Management Service templates
{: #kms-template}

   <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-key-management-service</code></td>
      <td>Create an {{site.data.keyword.cos_full_notm}} service instance with a bucket to store your data and provide a key management service resource for Hyper Protect Crypto Services and Key Protect service instance with a root key. This allow access between these services with an IBM Cloud Identity and Access Management policy.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_kms_key</code></li><li style="margin:0px; padding:0px"><code>ibm_kp_key</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-kms"><img src="/images/viewgithub.png"></a><br><br><a href="https://test.cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-kms&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  </tbody>
  </table>

## Kubernetes templates
{: #kubernetes-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
   <td><code>ibm-cluster-update</code></td>
      <td> Cordon and drain your worker nodes to update the IBM Cloud Kubernetes Service cluster master and worker nodes to the latest version.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>null_resource</code></li><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-cluster-update)</td>
  </tr>
  <tr>
   <td><code>cluster-worker-pool-zone</code></td>
      <td>Create an IBM Cloud Kubernetes Service cluster with a default worker pool that is spread across two zones. Also, you create another worker pool and bind an IBM Cloud service of your choice to the cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li><li style="margin:0px; padding:0px"><code>ibm_container_worker_pool_zone_attachment</code></li><li style="margin:0px; padding:0px"><code>ibm_container_worker_pool</code></li><li style="margin:0px; padding:0px"><code>ibm_service_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_service_key</code></li><li style="margin:0px; padding:0px"><code>ibm_container_bind_service</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-cluster/cluster-worker-pool-zone) </td>
  </tr>
 <tr>
   <td><code>vpc-classic-cluster</code></td>
      <td>Create an {{site.data.keyword.containerfull_notm}} cluster in a Virtual Private Cloud (VPC) for Generation 1 compute with worker nodes in a default worker pool that you spread across two zones. You can provision an IBM Cloud Object Storage service, and bind this service to the cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><listyle="margin:0px; padding:0px"><code>ibm_is_vpc</code></li><li style="margin:0px; padding:0px"><code>ibm_is_subnet</code></li><li style="margin:0px; padding:0px"><code>ibm_container_vpc_cluster</code></li><li style="margin:0px; padding:0px"><code>ibm_container_vpc_worker_pool</code></li><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_container_bind_service</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-cluster/vpc-classic-cluster)</td>
  </tr>
  <tr>
   <td><code>vpc-gen2-cluster</code></td>
      <td>Create an {{site.data.keyword.containerfull_notm}} cluster in a Virtual Private Cloud (VPC) for Generation 2 compute with worker nodes in a default worker pool that you spread across two zones. Also, you provision an IBM Cloud Object Storage service, and bind this service to the cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li><li style="margin:0px; padding:0px"><code>ibm_is_subnet</code></li><li style="margin:0px; padding:0px"><code>ibm_container_vpc_cluster</code></li><li style="margin:0px; padding:0px"><code>ibm_container_vpc_worker_pool</code></li><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_container_bind_service</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-cluster/vpc-gen2-cluster)</td>
  </tr>
   <tr>
    <td><code>ibm-iks-classic-ROKS</code></td>
      <td>Create a Red Hat View GitHub repository on IBM Cloud cluster that runs version 3.11 of the View GitHub repository Container Platform.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-iks-classic-ROKS)</td>
  </tr>
  <tr>
    <td><code>ibm-storage-cos</code></td>
      <td>Set up Helm in an {{site.data.keyword.containerlong_notm}} cluster to install the {{site.data.keyword.cos_full_notm}} Helm plug-in. Then, you create an {{site.data.keyword.cos_full_notm}} service instance where you can store data from the apps in your cluster. You also learn how to create a Kubernetes persistent volume claim (PVC) to create a bucket in your {{site.data.keyword.cos_full_notm}} instance. Also to deploy an app in the cluster that mounts your {{site.data.keyword.cos_full_notm}} bucket.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_container_bind_service</code></li><li style="margin:0px; padding:0px"><code>kubernetes_secret</code></li></ul></td>
       <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-storage-cos)</td>
  </tr>
  <tr>
    <td><code>ibm-openshift-job</code></td>
      <td>Create and execute a secured shell script in an {{site.data.keyword.openshiftlong_notm}} cluster by using a {[provider]} template. This template creates a Kubernetes configmap that includes a reference to a shell script. Then, you create a pod that mounts the configmap as a volume and executes the shell script.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>kubernetes_secret</code></li><li style="margin:0px; padding:0px"><code>kubernetes_config_map</code></li><li style="margin:0px; padding:0px"><code>kubernetes_job</code></li></ul></td>
       <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-openshift-job)</td>
  </tr>
  <tr>
    <td><code>portworx</code></td>
      <td>Set up Helm in an {{site.data.keyword.containerlong_notm}} software-defined storage (SDS) cluster to install Portworx as a storage solution. Make sure that this template requires an SDS cluster on Bare Metal worker nodes. After you installed Portworx, you can create persistent volume claims (PVC) to store data on local storage of your worker nodes. For more information, about Portworx and how to create an SDS cluster, see [Storing data on SDS with Portworx](/docs/containers?topic=containers-portworx).<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>random_id</code></li><li style="margin:0px; padding:0px"><code>kubernetes_secret</code></li><li style="margin:0px; padding:0px"><code>helm_release</code></li>
    </ul></td>
      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/portworx)</td>
  </tr>
    <tr>
    <td><code>ibm-lbaas</code></td>
      <td>Create an {{site.data.keyword.loadbalancer_full}} for a classic virtual server instance. You configure the load balancer to manage incoming HTTPS and HTTP network traffic and set up health monitoring for your virtual server instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_ssl_certificate</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_lbaas</code></li></li><li style="margin:0px; padding:0px"><code>ibm_lbaas_server_instance_attachment</code></li><li style="margin:0px; padding:0px"><code>ibm_lbaas_health_monitor</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-lbaas)</td>
  </tr> 
     <tr>
    <td><code>ibm-logdna-cluster-integration</code></td>
      <td>Create an IBM Cloud cluster integration service to configure IBM Cloud provider such as Helm, Kubernetes. Then, you can use a  resource role binding to fetch resource key, and agents to log through resource role binding.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>random_id</code></li><li style="margin:0px; padding:0px"><code>kubernetes_role_binding</code></li><li style="margin:0px; padding:0px"><code>helm_release</code></li></ul></td>
    <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-logdna-cluster-integration)</td>
  </tr>
  </tbody>
  </table>

## Object Storage templates
{: #cos-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
   <tr>
     <td><code>ibm-cos-bucket</code></td>
      <td>Create an [IBM Cloud Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-about-cloud-object-storage) service instance in IBM Cloud and your first bucket to persistently store data.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_group</code></li><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_cos_bucket</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-cos-bucket)</td>
  </tr>
  </tbody>
  </table>
  
## Power Systems templates
{: #power-sys-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
 <tr>
    <td><code>ibm-power</code></td>
      <td>Create an {{site.data.keyword.powerSys_notm}} instance with a public and a private network that mounts the system volumes. You can also create an SSH key to access the instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_pi_key</code></li><li style="margin:0px; padding:0px"><code>ibm_pi_network</code></li><li style="margin:0px; padding:0px"><code>ibm_pi_volume</code></li><li style="margin:0px; padding:0px"><code>ibm_pi_instance</code></li></ul></td>
   <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-power)</td>
  </tr>
  </tbody>
  </table>

## Resource Management templates
{: #resource-mgt-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-resource-instance</code></td>
      <td>Create an {{site.data.keyword.cos_full_notm}} service instance with HMAC credentials, and configure custom timeouts for creating, updating, or deleting the instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm-resource-instance</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-resource-instance)</td>
  </tr>
  </tbody>
  </table>

## Schematics templates
{: #schematics-template}

   <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
 <tr>
    <td><code>ibm-schematics</code></td>
      <td>Retrieve the {[provider]} state file and output variables for a {{site.data.keyword.bpshort}} workspace by using a {{site.data.keyword.bpshort}} data source. For more information, about how to use the data source, see [Managing cross-workspace state access with {[provider]}](/docs/schematics?topic=schematics-remote-state).<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>N/A</code></li></ul></td>
       <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-schematics)</td>
  </tr>
   </tbody>
  </table>
  
## Transit Gateway templates
{: #transit-gwy-template}

   <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-transit-gateway</code></td>
      <td>Create a transit gateways, list available connections, and locations for the gateways.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_tg_gateway</code></li><li style="margin:0px; padding:0px"><code>ibm_tg_connection</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li></ul></td>
      <td><a href="https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-transit-gateway"><img src="/images/viewgithub.png"></a><br><br><a href="https://test.cloud.ibm.com/schematics/workspaces/create?repository=https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-transit-gateway&terraform_version=terraform_v0.12"><img src="/images/deploytoschematics.png"></a></td>
  </tr>
  </tbody>
  </table>

## VPC infrastructure templates (Gen 1 compute)
{: #vpc-gen1-template}

  <table>
    <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-is-vpc</code></td>
      <td>Create a Virtual Private Cloud (VPC) for Generation 1 compute, configure a VPC load balancer with custom routing rules. Then, add a virtual server instance to your VPC that you can access from the internet by using a public IP address. Then, create another VPC Gen 1 and configure it with a VPN gateway with custom IPsec and IKE networking rules. You also learn how to create VPC Gen 1 block storage volumes.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpc_route</code></li><li style="margin:0px; padding:0px"><code>ibm_is_subnet</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb_listener</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb_listener_policy</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb_listener_policy_rule</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpn_gateway</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpn_gateway_connection</code></li><li style="margin:0px; padding:0px"><code>ibm_is_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_is_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_is_floating_ip</code></li><li style="margin:0px; padding:0px"><code>ibm_is_security_group_rule</code></li><li style="margin:0px; padding:0px"><code>ibm_is_ipsec_policy</code></li><li style="margin:0px; padding:0px"><code>ibm_is_ike_policy</code></li><li style="margin:0px; padding:0px"><code>ibm_is_volume</code></li><li style="margin:0px; padding:0px"><code>ibm_is_public_gateway</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-is-vpc)</td>
  </tr>
  </tbody>
  </table>

## VPC infrastructure templates (Gen 2 compute)
{: #vpc-gen2-template}

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ibm-is-ng</code></td>
      <td>Create a Virtual Private Cloud (VPC) for Generation 2 compute, configure a VPC load balancer with custom routing rules. Then, add a virtual server instance to your VPC that you can access from the internet by using a public IP address. Then, create another VPC Gen 2 and configure it with a VPN gateway with custom IPsec and IKE networking rules. You also learn how to create VPC Gen 2 block storage volumes.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpc_route</code></li><li style="margin:0px; padding:0px"><code>ibm_is_subnet</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb_listener</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb_listener_policy</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb_listener_policy_rule</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpn_gateway</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpn_gateway_connection</code></li><li style="margin:0px; padding:0px"><code>ibm_is_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_is_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_is_floating_ip</code></li><li style="margin:0px; padding:0px"><code>ibm_is_security_group_rule</code></li><li style="margin:0px; padding:0px"><code>ibm_is_ipsec_policy</code></li><li style="margin:0px; padding:0px"><code>ibm_is_ike_policy</code></li><li style="margin:0px; padding:0px"><code>ibm_is_volume</code></li><li style="margin:0px; padding:0px"><code>ibm_is_public_gateway</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/IBM-Cloud/terraform-provider-ibm/tree/master/examples/ibm-is-ng)</td>
  </tr>
  </tbody>
  </table>
  

## {{site.data.keyword.openshiftshort}} cluster templates
{: #openshift-cluster-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>openshift-dev-cluster</code></td>
      <td>Create an {{site.data.keyword.openshiftshort}} cluster and an Eclipse environment to install {{site.data.keyword.cloud_notm}}, code ready workspace, and pipeline operators.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li><li style="margin:0px; padding:0px"><code>null_resource</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/openshift-dev-cluster)</td>
  </tr>
  </tbody>
  </table>

## Ansible App deployment templates
{: #ansible-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ansible-app-deploy</code></td>
      <td>Deploy the {{site.data.keyword.vsi_is_short}} environment with SSH access and bastion host for {{site.data.keyword.redhat_notm}} Ansible in {{site.data.keyword.bpfull_notm}}.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>local_file</code></li><li style="margin:0px; padding:0px"><code>null_resource</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/ansible-app-deploy)</td>
  </tr>
  </tbody>
  </table>

## Multitier-vpc-bastion-host
{: #multitier-vpc-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>multitier-vpc-bastion-host</code></td>
      <td>Create a {{site.data.keyword.vsi_is_short}} for Generation 2 compute, configure a VPC load balancer, load balancer pool with a bastion host and secured SSH access. Then, install remote software by using {[provider]} or {{site.data.keyword.redhat_notm}} Ansible in {{site.data.keyword.bpfull_notm}}.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_instance</code></li><li style="margin:0px; padding:0px"><code>null_resource</code></li><li style="margin:0px; padding:0px"><code>ibm_is_security_group_rule</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb_listener</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb_pool</code></li><li style="margin:0px; padding:0px"><code>ibm_is_lb_pool_member</code></li><li style="margin:0px; padding:0px"><code>ibm_is_security_group</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/multitier-vpc-bastion-host)</td>
  </tr>
  </tbody>
  </table>

## LEMP
{: #lemp-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>LEMP</code></td>
      <td>Provision a classic virtual server instance in {{site.data.keyword.bplong_notm}}. Then, you can configure the instance with the components of LEMP stack such as LINUX, NGINX, MySQL (MariaDB), PHP through SSH keys.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>N/A</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/LEMP)</td>
  </tr>
  </tbody>
  </table> 

## openshift-cluster
{: #openshift-cluster}
 
<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>openshift-cluster</code></td>
      <td>Deploy an {{site.data.keyword.containerlong_notm}} in {{site.data.keyword.openshiftshort}} cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li><li style="margin:0px; padding:0px"><code>random_id</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/openshift-cluster)</td>
  </tr>
  </tbody>
  </table>

 ## fs2020
 {: #fs2020-template}
 
<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>fs2020</code></td>
      <td>Create an {{site.data.keyword.vpc_short}}, set up two zones each with a subnet, and place a virtual instance in each subnet. Then, you can deploy a load balancer to the server, and run a script to install NGINX to display the HTTPS response.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpc_address_prefix</code></li><li style="margin:0px; padding:0px"><code>ibm_is_subnet</code></li><li style="margin:0px; padding:0px"><code>ibm_is_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_is_floating_ip</code></li><li style="margin:0px; padding:0px"><code>ibm_is_security_group_rule</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/fs2020)</td>
  </tr>
  </tbody>
  </table>

 ## {[provider]}-ibm-awx
 {: #ibm-awx-template}
  
  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>terraform-ibm-awx</code></td>
      <td>Provision a secured `AWX` on {{site.data.keyword.vpc_full}} and execute a script to install Ansible, docker, and Git latest version. Then, you can access floating IP address of your virtual server instance. Pricing for Virtual Servers depends on the flavor of the instances.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>null_resource</code></li><li style="margin:0px; padding:0px"><code>tls_private_key</code></li><li style="margin:0px; padding:0px"><code>ibm_is_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_is_public_gateway</code></li><li style="margin:0px; padding:0px"><code>ibm_is_subnet</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li><li style="margin:0px; padding:0px"><code>ibm_is_security_group</code></li><li style="margin:0px; padding:0px"><code>ibm_is_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_is_security_group_rule</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/terraform-ibm-awx)</td>
  </tr>
  </tbody>
 </table>

 
 ## Cloud-Foundry-App 
 {: #cloud-foundry-template}
   
  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>Cloud-Foundry-App</code></td>
      <td>Provision and manage an IBM Cloud Foundry application with the source code of an application.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_app</code></li><li style="margin:0px; padding:0px"><code>ibm_app_route</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/Cloud-Foundry-App)</td>
  </tr>
  </tbody>
  </table>
  
## 2-zone-vpc
{: #2zone-vpc-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>2-zone-vpc</code></td>
      <td>Create two {{site.data.keyword.vpc_short}} in two separate zones and manage the infrastructure by using secured key and a VPN gateway connection.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>random_id</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li><li style="margin:0px; padding:0px"><code>ibm_is_subnet</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpn_gateway</code></li><li style="margin:0px; padding:0px"><code>ibm_is_vpn_gateway_connection</code></li><li style="margin:0px; padding:0px"><code>ibm_is_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_is_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_is_floating_ip</code></li><li style="margin:0px; padding:0px"><code>ibm_is_security_group_rule</code></li><li style="margin:0px; padding:0px"><code>ibm_is_ipsec_policy</code></li><li style="margin:0px; padding:0px"><code>ibm_is_ike_policy</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/2-zone-vpc)</td>
  </tr>
  </tbody>
  </table>
  
## VSI-database 
{: #vsi-db-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>VSI-database</code></td>
      <td>Create an {{site.data.keyword.cloud_notm}} classic {{site.data.keyword.BluVirtServers_short}} with a PostgreSQL database instance. Then, the {{site.data.keyword.cloud_notm}} automatically configures security groups to connect virtual server with a database port.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_database</code></li><li style="margin:0px; padding:0px"><code>ibm_is_security_group_rule</code></li><li style="margin:0px; padding:0px"><code>ibm_security_group</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/VSI-database)</td>
  </tr>
  </tbody>
  </table>
  
## LAMP 
{: #lamp-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>LAMP</code></td>
      <td>Provision a classic virtual server instance in {{site.data.keyword.bplong_notm}}. Then, you can configure the instance with the components of LAMP stack such as Linux, Apache, MySQL (MariaDB), PHP through SSH keys.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/LAMP)</td>
  </tr>
  </tbody>
  </table>
  
## terraform_modules
{: #terraform-module}
  
<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>terraform_modules</code></td>
      <td>Develop a {[provider]} modules, that, can be used across payloads. Then, provision a cluster virtual machine in {{site.data.keyword.cloud_notm}} and run scripts to install software, and delete temporary keys.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>N/A</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/terraform-modules)</td>
  </tr>
  </tbody>
  </table>

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>cloud-service</code></td>
      <td>Create an {{site.data.keyword.cloud_notm}} environment to separate software components into development tiers such as staging, QA, and production.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_service_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_service_key</code></li><li style="margin:0px; padding:0px"><code>random_pet</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/cloud-service)</td>
  </tr>
  </tbody>
  </table>

## MongoDB
{: #mongodb-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>mongodb</code></td>
      <td>Deploy a MongoDB server on an IBM VSI virtual machine with a secured SSH key.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/mongodb)</td>
  </tr>
  </tbody>
  </table>
  
## ssh-key
{: #sshkey-template}

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>ssh-key</code></td>
      <td>Create an SSH key in an {{site.data.keyword.cloud_notm}} account.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/ssh-key)</td>
  </tr>
  </tbody>
  </table>## logDNA

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>logDNA</code></td>
      <td>Create an {{site.data.keyword.cloud_notm}} classic virtual machine to deploy a LogDNA logsource on Linux and Ubuntu. <br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/logDNA)</td>
  </tr>
  </tbody>
  </table>
  
 ## Container-multi-az-cluster 

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>container-multi-az-cluster</code></td>
      <td>Create a Multi-AZ cluster environment with the two worker pools and a subnet to synchronously replicate the data in a different availability zone.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_network_vlan</code></li><li style="margin:0px; padding:0px"><code>ibm_subnet</code></li><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li><li style="margin:0px; padding:0px"><code>ibm_container_worker_pool</code></li><li style="margin:0px; padding:0px"><code>ibm_container_worker_pool_zone_attachment</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/container-multi-az-cluster)</td>
  </tr>
  </tbody>
  </table>
  
 ## `Hpc-fss-cluster`

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
  <tr>
    <td><code>hpc-fss-cluster</code></td>
      <td>Create a High Performance Computing (HPC) and FSS cluster with an IBM Spectrum Symphony CWS/LSF Cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_compute_ssh_key</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_vm_instance</code></li><li style="margin:0px; padding:0px"><code>ibm_compute_bare_metal</code></li></ul></td>
     <td>[View GitHub repo](https://github.com/Cloud-Schematics/hpc-fss-cluster)</td>
  </tr>
  </tbody>
  </table>
</staging>