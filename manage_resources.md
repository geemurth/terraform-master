---

copyright:
  years: 2017, [{CURRENT_YEAR}]
lastupdated: "[{LAST_UPDATED_DATE}]"

keywords: Add resources, remove resources, iaas, softlayer, ibm cloud resources, ibm cloud services, {[provider]}, provision resources

subcollection: terraform

---

{[headtag.md]}


# Managing IBM Cloud resources with {[provider]}
{: #manage_resources}

Use the {[provider]} CLI to create your platform and infrastructure resources in {{site.data.keyword.cloud_notm}}. 
{: shortdesc}

## Provisioning IBM Cloud resources
{: #provision_resources}

To provision {{site.data.keyword.cloud_notm}} resources, you must describe the state of your resources that you want to achieve in a configuration file.  
{: shortdesc}

{[provider]} configuration files are written by using the [HashiCorp Configuration Language (HCL) ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.terraform.io/docs/configuration/syntax.html) or JSON syntax. When you create your configuration file, you must describe the type of resource that you want and the state that you want to achieve for your resource. {[provider]} reads this configuration and creates an execution plan with the steps that were identified to achieve the specified state. If existing resources are found, {[provider]} identifies the necessary steps to update them. 

Before you begin: 
- [Install the {[provider]} CLI and the {{site.data.keyword.cloud_notm}} Provider plug-in](/docs/terraform?topic=terraform-setup_cli#setup_cli).
- [Configure the {{site.data.keyword.cloud_notm}} Provider plug-in to use your {{site.data.keyword.cloud_notm}} credentials](/docs/terraform?topic=terraform-setup_cli#configure_provider). 

The following example shows how you can configure a virtual server in {{site.data.keyword.cloud_notm}} by using JSON syntax. A virtual server is an {{site.data.keyword.cloud_notm}} infrastructure resource that incurs costs. Be sure to review [available plans ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/catalog/infrastructure/virtual-server-group) before you proceed. 
{: important} 

Looking for other resource types? Find a complete list of supported resource types in the [{{site.data.keyword.cloud_notm}} Provider plug-in reference](/docs/terraform?topic=terraform-setup_cli#configure_provider). 
{: tip}

1. Create a configuration file that is named `sample.tf` with the following content. Configuration file names must have the `.tf` extension to be found by {[provider]}. Store this file in the same folder that you used to store your {{site.data.keyword.cloud_notm}} credentials. 
   ```
   resource "ibm_compute_vm_instance" "vm1" {
    hostname = "vm1"
    domain = "example.com"
    os_reference_code = "DEBIAN_8_64"
    datacenter = "dal09"
    network_speed = 10
    hourly_billing = true
    private_network_only = false
    cores = 1
    memory = 1024
    disks = [25]
    local_disk = false
   }
   ```
   {: codeblock}
   
2. Initialize {[provider]}. 
   ```
   terraform init
   ```
   {: pre}
   
   Example output: 
   ```
   Initializing provider plugins...

   The following providers do not have any version constraints in configuration, so the latest version was installed.

   To prevent automatic upgrades to new major versions that may contain breaking changes, it is recommended to add version = "..." constraints to the corresponding provider blocks in configuration, with the constraint strings suggested.

   * provider.ibm: version = "~> 0.11"

   {[provider]} has been successfully initialized!

   You may now begin working with {[provider]}. Try running "terraform plan" to see any changes that are required for your infrastructure. All {[provider]} commands should now work.

   If you ever set or change modules or backend configuration for {[provider]}, rerun this command to reinitialize your working directory. If you forget, other commands detects it and remind you to do so if necessary.
   ```
   {: screen}
   
3. Generate a {[provider]} execution plan. When you execute this command, {[provider]} validates the syntax of your configuration file and resource definitions against the specifications that are provided by the {{site.data.keyword.cloud_notm}} Provider plug-in. 
   ```
   terraform plan
   ```
   {: pre}

   Example output:
   ```
   Refreshing {[provider]} state in-memory prior to plan...
   The refreshed state be used to calculate this plan, but not be persisted to local or remote state storage.

   An execution plan has been generated and is shown here.
   Resource actions are indicated with the following symbols:
     + create

   {[provider]} perform the following actions:

     + ibm_compute_vm_instance.vm1
         id:                           <computed>
         block_storage_ids.#:          <computed>
         cores:                        "1"
         datacenter:                   "dal09"
         disks.#:                      "1"
         disks.0:                      "25"
         domain:                       "example.com"
         file_storage_ids.#:           <computed>
         hostname:                     "vm1"
         hourly_billing:               "true"
         ip_address_id:                <computed>
         ip_address_id_private:        <computed>
         ipv4_address:                 <computed>
         ipv4_address_private:         <computed>
         ipv6_address:                 <computed>
         ipv6_address_id:              <computed>
         ipv6_enabled:                 "false"
         ipv6_static_enabled:          "false"
         local_disk:                   "false"
         memory:                       "1024"
         network_speed:                "10"
         os_reference_code:            "DEBIAN_8_64"
         private_interface_id:         <computed>
         private_network_only:         "false"
         private_security_group_ids.#: <computed>
         private_subnet:               <computed>
         private_subnet_id:            <computed>
         private_vlan_id:              <computed>
         public_bandwidth_limited:     <computed>
         public_bandwidth_unlimited:   "false"
         public_interface_id:          <computed>
         public_ipv6_subnet:           <computed>
         public_ipv6_subnet_id:        <computed>
         public_security_group_ids.#:  <computed>
         public_subnet:                <computed>
         public_subnet_id:             <computed>
         public_vlan_id:               <computed>
         secondary_ip_addresses.#:     <computed>
         wait_time_minutes:            "90"

   Plan: 1 to add, 0 to change, 0 to destroy.
   ------------------------------------------------------------------------
   **Note** You didn't specify an "-out" parameter to save this plan, so {[provider]} can't guarantee that exactly these actions be performed if "terraform apply" is subsequently run.
   ```
   {: screen}
   
4. Review the execution plan to verify the steps that were identified by {[provider]} to provision the virtual server.  

5. Create your infrastructure resources.  
   ```
   terraform apply
   ```
   {: pre} 
   
   Confirm the creation of infrastructure resources by entering **yes** when prompted. 
   
   Example output: 
   ```
   Creating...
     block_storage_ids.#:        "" => "<computed>"
     cores:                      "" => "1"
     datacenter:                 "" => "dal09"
     disks.#:                    "" => "1"
     disks.0:                    "" => "25"
     domain:                     "" => "example.com"
     file_storage_ids.#:         "" => "<computed>"
     hostname:                   "" => "vm1"
     hourly_billing:             "" => "true"
     ip_address_id:              "" => "<computed>"
     ip_address_id_private:      "" => "<computed>"
     ipv4_address:               "" => "<computed>"
     ipv4_address_private:       "" => "<computed>"
     ipv6_address:               "" => "<computed>"
     ipv6_address_id:            "" => "<computed>"
     ipv6_enabled:               "" => "false"
     local_disk:                 "" => "false"
     memory:                     "" => "1024"
     network_speed:              "" => "10"
     os_reference_code:          "" => "DEBIAN_8_64"
     private_network_only:       "" => "false"
     private_subnet:             "" => "<computed>"
     private_vlan_id:            "" => "<computed>"
     public_bandwidth_limited:   "" => "<computed>"
     public_bandwidth_unlimited: "" => "false"
     public_ipv6_subnet:         "" => "<computed>"
     public_subnet:              "" => "<computed>"
     public_vlan_id:             "" => "<computed>"
     secondary_ip_addresses.#:   "" => "<computed>"
     wait_time_minutes:          "" => "90"
   ibm_compute_vm_instance.vm1: Still creating... (10s elapsed)
   ibm_compute_vm_instance.vm1: Still creating... (20s elapsed)
   ibm_compute_vm_instance.vm1: Still creating... (30s elapsed)
   ibm_compute_vm_instance.vm1: Still creating... (40s elapsed)
   ibm_compute_vm_instance.vm1: Still creating... (50s elapsed)
   ibm_compute_vm_instance.vm1: Still creating... (1m0s elapsed)
   ibm_compute_vm_instance.vm1: Creation complete after 1m04s (ID: 62364997)

   Apply complete! Resources: 1 added, 0 changed, 0 destroyed.
   ```
   {: screen}
   
   
## Updating IBM Cloud resources
{: #update_resources}

You can update your resources by changing your {[provider]} configuration file and applying these changes in your environment. 
{: shortdesc}

1. List your {{site.data.keyword.cloud_notm}} resources. 
   ```
   terraform show
   ```
   {: pre}
   
   Example output: 
   ```
   ibm_compute_vm_instance.vm1:
     id = 62364997
     block_storage_ids.# = 0
     cores = 1
     datacenter = dal09
     dedicated_acct_host_only = false
     disks.# = 1
     disks.0 = 25
     domain = example.com
     file_storage_ids.# = 0
     hostname = vm1
     hourly_billing = true
     ip_address_id = 119153307
     ip_address_id_private = 119154963
     ipv4_address = 169.46.192.34
     ipv4_address_private = 10.173.135.134
     ipv6_enabled = false
     ipv6_static_enabled = false
     local_disk = false
     memory = 1024
     network_speed = 10
     notes = 
     os_reference_code = DEBIAN_8_64
     private_interface_id = 35066699
     private_network_only = false
     private_security_group_ids.# = 0
     private_subnet = 10.173.135.128/26
     private_subnet_id = 1304363
     private_vlan_id = 2433445
     public_bandwidth_unlimited = false
     public_interface_id = 35066701
     public_security_group_ids.# = 0
     public_subnet = 169.46.192.32/28
     public_subnet_id = 1810073
     public_vlan_id = 2433443
     secondary_ip_addresses.# = 0
     wait_time_minutes = 90
   ```
   {: screen}
   
2. Open your `sample.tf` configuration file and change a value. For example, you can change the **network_speed** to **100**. To find an overview of parameters that you can change, see the [{{site.data.keyword.cloud_notm}} resource reference](/docs/terraform?topic=terraform-setup_cli#configure_provider).
   
3. Create a {[provider]} execution plan. 
   ```
   terraform plan
   ```
   {: pre}
   
   Example output: 
   ```
   Refreshing {[provider]} state in-memory prior to plan...
   The refreshed state be used to calculate this plan, but not be persisted to local or remote state storage.

   ibm_compute_vm_instance.vm1: Refreshing state... (ID: 51404681)

   ---------------------------------------------------------------

   An execution plan has been generated and is shown here.
   Resource actions are indicated with the following symbols:
    ~ update in-place

   {[provider]} performs the following actions:

    ~ ibm_compute_vm_instance.vm1
    network_speed: "10" => "100"

   Plan: 0 to add, 1 to change, 0 to destroy.
   ```
   {: screen}
   
4. Apply the changes to your {{site.data.keyword.cloud_notm}} resources. 
   ```
   terraform apply
   ```
   {: pre}
   
5. Verify that your {{site.data.keyword.cloud_notm}} resources are updated. 
   ```
   terraform show
   ```
   {: pre}

## Removing IBM Cloud resources 
{: #remove_resources}

You can use {[provider]} to remove {{site.data.keyword.cloud_notm}} resources if you do not want them anymore. 
{: shortdesc}

1. Show the summary of steps that {[provider]} identified to remove your {{site.data.keyword.cloud_notm}} resources. 
   ```
   terraform plan -destroy
   ```
   {: pre}
   
2. Verify the {[provider]} execution plan. 
3. Remove your {{site.data.keyword.cloud_notm}} resources. 
   ```
   terraform destroy
   ```
   {: pre}
   
   Example output: 
   ```
   ibm_compute_vm_instance.vm1: Refreshing state... (ID: 60948867)
   An execution plan has been generated and is shown here.
   Resource actions are indicated with the following symbols:
     - destroy

   {[provider]} performs the following actions:

     - ibm_compute_vm_instance.vm1

   Plan: 0 to add, 0 to change, 1 to destroy.

   Do you really want to destroy?
     {[provider]} destroys all your managed infrastructure, as shown above.
     There is no undo. Only 'yes' is accepted to confirm.

     Enter a value: yes

   ibm_compute_vm_instance.vm1: Destroying... (ID: 60948867)
   ibm_compute_vm_instance.vm1: Still destroying... (ID: 60948867, 10s elapsed)
   ibm_compute_vm_instance.vm1: Destruction complete after 14s
   Destroy complete! Resources: 1 destroyed.
   ```
   {: screen}
   
4. Verify that your {{site.data.keyword.cloud_notm}} resources are removed. 
   ```
   terraform show
   ```
   {: pre}
   