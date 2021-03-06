---

copyright:
  years: 2017, [{CURRENT_YEAR}]
lastupdated: "[{LAST_UPDATED_DATE}]"

keywords: terraform provider plugin, terraform api gateway

subcollection: terraform

---

{[headtag.md]}

# API Gateway data sources
{: #api-gw-data-sources}

Review the data sources that you can use to retrieve information about your API Gateway resources. All data sources are imported as read-only information. You can reference the output parameters for each data source by using {[provider]} interpolation syntax.

{[provider-param-data-source.md]}

## `ibm_api_gateway`
{: #api-gw}

Retrieve information about an existing API Gateway instance. 
{: shortdesc}

### Sample {[provider]} code
{: #api-gw-sample}

```
data "ibm_api_gateway" "apigateway" {
    service_instance_crn = ibm_resource_instance.apigateway.id
    
}
```
{: codeblock}

### Input parameters
{: #api-gw-input}

Review the input parameters that you can specify for your resource. 
{: shortdesc}

| Input parameter | Data type | Required / optional | Description |
| ------------- |-------------| ----- | -------------- |
|`service_instance_crn`|String|Required|The CRN of the API Gateway service instance. |


### Output parameters
{: #api-gw-output}

Review the output parameters that you can access after your resource is created. 
{: shortdesc}

| Output parameter | Data type | Description |
| ------------- |-------------| -------------- |
|`endpoints`|List of API Gateway endpoints|A list of API Gateway endpoints that are associated with the service instance.|
|`endpoints.endpoint_id`|String|The ID of the endpoint.|
|`endpoints.name`|String|The name of the endpoint.|
|`endpoints.managed`|Boolean|If set to **true**, the endpoint is online. If set to **false**, the endpoint is offline.|
|`endpoints.shared`|String|The shared status of the endpoint.|
|`endpoints.base_path`|String|The base path of the endpoint.|
|`endpoints.routes`|Array of strings|A list of routes that can be invoked for the endpoint.|
|`endpoints.provider_id`|String|The provider ID of the endpoint.|
|`endpoints.managed_url`|String|The managed URL of an endpoint.|
|`endpoints.alias_url`|String|The alias URL of an endpoint.|
|`endpoints.open_api_doc`|String|The Open API document of the endpoint.|
|`endpoints.subscriptions`|List of endpoint subscriptions|A list of subscriptions that you created for your endpoint.|
|`endpoints.subscriptions.client_id`|String|The client ID of a subscription.|
|`endpoints.subscriptions.name`|String|The name of the subscription.|
|`endpoints.subscriptions.type`|String|The type of subscription. Supported values are `bluemix` and `external`.|
|`endpoints.subscriptions.secret_provided`|Boolean|If set to **true**, the client secret is provided. If set to **false**, the client secret is not provided.|
