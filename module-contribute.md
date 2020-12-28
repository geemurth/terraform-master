<staging>
---

copyright:
  years: 2017, [{CURRENT_YEAR}]
lastupdated: "[{LAST_UPDATED_DATE}]"

keywords: modules contribution, softlayer, iaas

subcollection: terraform

---

{[headtag.md]}

# Contribute and publish into {[provider]} modules
{: #contribute-modules}

The requirements for publishing a repository is extremely easy when adhered to the requirements are natural. The table states guidelines to contribute to an existing {[provider]} modules repository or creating a new repository in terraform-ibm-modules organisation.
{: shortdesc}

1. **GitHub** The modules must be on a public GitHub repository.
2. **Repository name {[provider]}** Module repositories must use three part name format, that reflects the type of infrastructure the module manages. The main provider creates the infrastructure. The segment can contain additional hyphen.
3. **Repository description** The GitHub repository must to populate with the short description.
4. **Release tags** Tags are used to identify module release and version. Release tag names must be a semantic version, that can optionally prefixed with `v`. For example, v1.0.0.
5. **Modules structure** The module must adhere to the standard module structure. For more information, refer [Module structure](https://github.com/terraform-ibm-modules/getting-started/blob/master/module_structure.md){: external}.
6. **Module inputs** The input variable names must be inline with the UI page of the input variables. This is to maintain the consistency while provisioning the resource with through {[provider]} module or UI. The input variables must have descriptions. You need to use `input.tfvars` as a file to configure any complex type constraints like `list`, `map`, etc. For more information, refer [Input variables](https://github.com/terraform-ibm-modules/getting-started/blob/master/input_variables.md){: external}.
7. **Optional input arguments** The module can include both mandatory and optional arguments. The optional arguments have a conditional check. You need to provide the default value for the arguments, which is used when the user does not provide the input values.
8. **Module output** Returns the results to the calling module. You can use this to populate arguments in other resources or modules. Output must have descriptions. For more information, refer [module output](https://github.com/terraform-ibm-modules/getting-started/blob/master/output_values.md){: external}.

</staging>