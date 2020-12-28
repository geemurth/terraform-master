<staging>
---

copyright:
  years: 2017, [{CURRENT_YEAR}]
lastupdated: "[{LAST_UPDATED_DATE}]"

keywords: terraform modules, schematics template, modules

subcollection: terraform

---


{[headtag.md]}


# Provisioning resources by using {[provider]} modules
{: #terraform-modules}

A {[provider]} module is a collection of resources that are combined and configured for reusability in multiple places throughout your code. In each {[provider]} configuration, you need to create one module. Sample {[provider]} modules with the examples are provided to seamlessly work in {{site.data.keyword.cloud_notm}}. For more information, about modules, refer [{[provider]} modules](https://www.terraform.io/docs/configuration/modules.html){: external}.
{: shortdesc}

All {[provider]} modules use the {[provider]} version 0.12 and later format.
{: note}

## Activity tracker
{: #activity-tracker}

Collection of modules that makes you easier to provision a activity tracker as a service on {{site.data.keyword.cloud_notm}} platform. For more information, about activity tracker, refer to [Activity tracker with LogDNA](/docs/Activity-Tracker-with-LogDNA?topic=Activity-Tracker-with-LogDNA-getting-started).

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:150px">Description and resources</th>
    <th style="width:150px">Access</th>
   </thead>
  <tbody>
    <tr>
      <td><code>activity_tracker</code></td>
      <td>Provision an activity tracker as a service.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cos/tree/master/modules/bucket)</td><br><br>
      <td>[View provisioning example](https://github.com/terraform-ibm-modules/terraform-ibm-cos/tree/master/examples/bucket) **Note** <br> 
       ```
       module "cos" 
       {
         source = "../../modules/cos_instance"
         name              = var.name
         resource_group_id = data.ibm_resource_group.cos_group.id
         plan              = var.plan
         location          = var.region
        }
        ```
      </td>
    </tr>
  </tbody>
  </table>
  {: caption="Activity tracker" caption-side="top"}

## Certificate manager
{: #certificate-manager}

Collection of modules that makes you easier to provision certificate manager, import and order certificates on {{site.data.keyword.cloud_notm}} platform. For more information, about certificate manager resources, refer to [Certificate manager resources](/docs/terraform?topic=terraform-cert-manager-resources).

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
    <tr>
      <td><code>ibm-cms-instance</code></td>
      <td>This module is used to create a certificate manager instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-certificate-manager/tree/main/modules/instance)</td>
 </tr>
    <tr>
      <td><code>ibm-cms-import</code></td>
      <td>This module import a certificate into the Certificate Manager service instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_certificate_manager_import</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-certificate-manager/tree/main/modules/import)</td>
 </tr>
    <tr>
      <td><code>ibm-cms-order</code></td>
      <td>This module import a certificate into the Certificate Manager service instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_certificate_manager_order</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-certificate-manager/tree/main/modules/order)</td>
 </tr>
  </tbody>
  </table>
  {: caption="Certificate manager" caption-side="top"}

## Cloud Object Storage
{: #cos-module}

This is a collection of modules that makes you easier to provision a {{site.data.keyword.cos_full_notm}} on {{site.data.keyword.cloud_notm}} platform.

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
    <tr>
      <td><code>cos-instance</code></td>
      <td>This module is used to create a {{site.data.keyword.cos_full_notm}} instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cos/tree/master/examples/instance)</td>
 </tr>
    <tr>
      <td><code>cos-bucket</code></td>
      <td>This module is used to create a {{site.data.keyword.cos_full_notm}} bucket.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_cos_bucket</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cos)</td>
 </tr>
  </tbody>
  </table>
  {: caption="Cloud object storage" caption-side="top"}


## Cluster
{: #cluster-module}

This is a collection of modules that makes you easier to provision a cluster on {{site.data.keyword.cloud_notm}} platform.

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
    <tr>
      <td><code>classic-free-cluster</code></td>
      <td>Create a classic free cluster module.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cluster/tree/master/modules/classic-free)</td>
     </tr>
          <tr>
      <td><code>classic-kubernetes-multi-zone-cluster</code></td>
      <td>Create a classic Kubernetes multi zone cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li><li style="margin:0px; padding:0px"><code>ibm_container_worker_pool_zone_attachment</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cluster/tree/master/modules/classic-kubernetes-multi-zone)</td>
     </tr>
    <tr>
      <td><code>classic-kubernetes-single-zone-cluster</code></td>
      <td>Create a classic Kubernetes single zone cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cluster/tree/master/modules/classic-kubernetes-single-zone)</td>
     </tr>
     <tr>
      <td><code>classic-openshift-multi-zone-cluster </code></td>
      <td>Create a classic OpenShift multi zone cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li><li style="margin:0px; padding:0px"><code>ibm_container_worker_pool_zone_attachment</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cluster/tree/master/modules/classic-openshift-multi-zone)</td>
     </tr>
    <tr>
      <td><code>classic-openshift-single-zone-cluster</code></td>
      <td>Create a classic OpenShift single zone cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_cluster</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cluster/tree/master/modules/classic-openshift-single-zone)</td>
     </tr>
    <tr>
      <td><code>vpc-kubernetes-cluster</code></td>
      <td>Create a VPC OpenShift Kubernetes cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_vpc_cluster</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cluster/tree/master/modules/vpc-kubernetes)</td>
     </tr>
    <tr>
      <td><code>vpc-openshift-cluster</code></td>
      <td>Create a VPC OpenShift cluster.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_vpc_cluster</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cluster/tree/master/modules/vpc-openshift)</td>
     </tr>
  </tbody>
  </table>
  {: caption="Cluster" caption-side="top"}

  The IBM cluster module also has the following other modules to configure already provisioned cluster in {{site.data.keyword.cloud_notm}} platform:

  <table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
   <tr>
      <td><code>configure-cluster: addons</code></td>
      <td>Configure cluster submodule to access add-ons module.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_addons</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cluster/tree/master/modules/configure-addons)</td>
    </tr>
     <tr>
      <td><code>configure-cluster: classic-cluster-worker-pool</code></td>
      <td>Configure cluster submodule to access classic cluster worker pool module.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_worker_pool</code></li><li style="margin:0px; padding:0px"><code>ibm_container_worker_pool_zone_attachment</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cluster/tree/master/modules/configure-classic-worker-pool)</td>
     </tr>
    <tr>
      <td><code>configure-cluster: vpc-cluster-worker-pool</code></td>
      <td>Configure cluster submodule to access vpc cluster worker pool module.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_container_vpc_worker_pool</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-cluster/tree/master/modules/configure-vpc-worker-pool)</td>
     </tr>
     </tbody>
  </table>
  {: caption="Cluster sub module" caption-side="top"}

## Database 
{: #database-module}

This is a collection of modules that makes you easier to provision a database on {{site.data.keyword.cloud_notm}} platform. For more information, about provisioning various databases resource, refer to [Database resources](/docs/terraform?topic=terraform-databases-resources).

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
    <tr>
      <td><code>ibm-elasticsearch</code></td>
      <td>Create an IBM Elastic search module.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_database</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-database/tree/main/modules/elasticsearch)</td>
     </tr>
          <tr>
      <td><code>ibm-etcd</code></td>
      <td>Create an IBM etcd module.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_database</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-database/tree/main/modules/etcd)</td>
     </tr>
    <tr>
      <td><code>ibm-mongo</code></td>
      <td>Create an IBM Mongo database module.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_database</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-database/tree/main/modules/mongo)</td>
     </tr>
     <tr>
      <td><code>ibm-postgresql</code></td>
      <td>Create an IBM PostgreSQL module.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_database</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-database/tree/main/modules/postgresql)</td>
     </tr>
    <tr>
      <td><code>ibm-rabbitmq</code></td>
      <td>Create an IBM RabbitMQ module.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_database</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-database/tree/main/modules/rabbitmq)</td>
     </tr>
    <tr>
      <td><code>ibm-redis</code></td>
      <td>Create an IBM Redis module.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_database</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-database/tree/main/modules/redis)</td>
    </tr>
  </tbody>
  </table>
  {: caption="Database" caption-side="top"}


## LogDNA 
{: #logdna-module}

This is a collection of modules that makes you easier to provision LogDNA on {{site.data.keyword.cloud_notm}} platform. For more information, about LogDNA, refer to [Analysis with LogDNA](/docs/Log-Analysis-with-LogDNA?topic=Log-Analysis-with-LogDNA-getting-started).

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
    <tr>
      <td><code>logdna_instance</code></td>
      <td>This module is used to create a logDNA instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-logdna/tree/main/modules/logdna_instance)</td>
 </tr>
    <tr>
      <td><code>logdna_instance_key</code></td>
      <td>This module is used to create a LogDNA instance key.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_key</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-logdna/tree/main/modules/instance-key)</td>
 </tr>
  </tbody>
  </table>
  {: caption="LogDNA" caption-side="top"}

## Sysdig
{: #sysdig-module}

This is a collection of modules that makes you easier to provision Sysdig monitor on {{site.data.keyword.cloud_notm}} platform. For more information, about monitoring with Sysdig, refer to [Monitoring with Sysdig](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-getting-started).

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and resources</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
    <tr>
      <td><code>sysdig_instance</code></td>
      <td>This module is used to create a logDNA instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_instance</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-sysdig/tree/main/modules/instance)</td>
 </tr>
    <tr>
      <td><code>sysdig_instance_key</code></td>
      <td>This module is used to create a LogDNA instance key.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_resource_key</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-sysdig/tree/main/modules/instance-key)</td>
 </tr>
  </tbody>
  </table>
  {: caption="Sysdig" caption-side="top"}

## VPC {[provider]} 
{: #vpc-module}

This is a collection of modules that makes you easier to provision a cluster on {{site.data.keyword.cloud_notm}} platform. For more information, about VPC infrastructure resource, refer to [VPC resources](/docs/terraform?topic=terraform-vpc-gen2-resources).

<table>
   <thead>
    <th style="width:60px">Name</th>
    <th style="width:250px">Description and module</th>
    <th style="width:150px">Access</th>
  </thead>
  <tbody>
      <tr>
      <td><code>vpc</code></td>
      <td>This module is used to create a VPC.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_vpc</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-vpc/tree/master/modules/vpc)</td>
    </tr>
    <tr>
      <td><code>vpc-address-prefix</code></td>
      <td>This module is used to create a VPC Address Prefix.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_vpc_address_prefix</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-vpc/tree/master/modules/configure-vpc/vpc-address-prefix)</td>
   </tr>
     <tr>
      <td><code>vpc-route</code></td>
      <td>This module is used to create a VPC Route.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_vpc_route</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-vpc/tree/master/modules/configure-vpc/vpc-route)</td>
 </tr>
      <tr>
      <td><code>subnet</code></td>
      <td>This module is used to create a Subnet.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_subnet</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-vpc/tree/master/modules/subnet)</td>
 </tr>
      <tr>
      <td><code>security-group</code></td>
      <td>This module is used to create a security group.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_security_group</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-vpc/tree/master/modules/security-group)</td>
 </tr>
   <tr>
      <td><code>floatingIP</code></td>
      <td>This module is used to create a floating IP.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_floating_ip</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-vpc/tree/master/modules/floatingIP)</td>
 </tr>
    <tr>
      <td><code>instance</code></td>
      <td>This module is used to create an instance.<br><br>**Resources**<br><ul style="margin:0px 0px 0px 20px; padding:0px"><li style="margin:0px; padding:0px"><code>ibm_is_instance</code></li></ul></td>
      <td>[View GitHub repo](https://github.com/terraform-ibm-modules/terraform-ibm-vpc/tree/master/modules/instance)</td>
 </tr>
   </tbody>
  </table>
  {: caption="VPC" caption-side="top"}

## Using the {[provider]} module in your templates
{: #how-to-use-module}

The {[provider]} modules for {{site.data.keyword.cloud_notm}} is a community source project. Refer to [Community source project](https://github.com/terraform-ibm-modules) for the details. The requirements for publishing or updating the module to this repository is extremely easy, when you follow these guidelines.

* GitHub repository - The modules must be on a public GitHub repository. The repository can include one or more modules. Each module support the ability to provision or configure the related {{site.data.keyword.cloud_notm}} resource, in more than one ways.
* Repository name - {[provider]} module repository must use three part name format, that reflects the type of {{site.data.keyword.cloud_notm}} resources the module manages.
* Repository description - {[provider]} module repository must include a short description of the capability supported by the module.
* Release tags - {[provider]} module release and version must be tagged. Release tag names must be a semantic version, that can optionally prefixed with `v`. For example, `v1.0.0`.
* Modules structure - {[provider]} module repository must follow the folder structure as described in the guidelines. Refer to [Module strucutre guidelines](https://github.com/terraform-ibm-modules/getting-started/blob/master/module_structure.md){: external} for the details. More than the modules, the repository must  include examples of how to use these modules.
* Module inputs - The input variable names and description of the {[provider]} modules must follow as described in the guidelines. Refer to [Module input guidelines](https://github.com/terraform-ibm-modules/getting-started/blob/master/input_variables.md){: external} for the details.
 - The input variable names must be similar to or same as the corresponding input parameters used to provision and configure the resource, using the {{site.data.keyword.cloud_notm}} console (GUI).
* Module outputs - The output variable names and description of the {[provider]} modules must follow as described in the guidelines. Refer to [Module outputs](https://github.com/terraform-ibm-modules/getting-started/blob/master/output_values.md) for the details.
 - The output of the {[provider]} module can be used as inputs by the other resources or modules in your {[provider]} template.

</staging>
