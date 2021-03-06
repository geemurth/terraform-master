---

copyright:
  years: 2017, [{CURRENT_YEAR}]
lastupdated: "[{LAST_UPDATED_DATE}]"

keywords: terraform provider plugin, terraform event streams, terraform event stream service, terraform event streams topic

subcollection: terraform

---

{[headtag.md]}

# Event Streams data sources
{: #event-streams-ds}


Review the [Event Streams](/docs/EventStreams?topic=EventStreams-about) resource that you can connect, administer, developed with event streams and integrate with the other services. You can reference the output parameters for each resource in other resources or data sources by using [{[provider]} interpolation syntax](https://www.terraform.io/docs/configuration/resources.html){: external}.
{: shortdesc}

{[provider-param-resource.md]}

## ibm_event_streams_topic
{: #event-streams-topic}

Import the name of an existing event streams topic as a read-only data source. Then, You can reference the fields of the data source in other resources within the same configuration by using interpolation syntax. 
{: shortdesc}

### Sample {[provider]} code
{: #event-stream-ds-sample}

```
data "ibm_resource_instance" "es_instance" {
  name              = "terraform-integration"
  resource_group_id = data.ibm_resource_group.group.id
}

data "ibm_event_streams_topic" "es_topic" {
  resource_instance_id = data.ibm_resource_instance.es_instance.id
  name                 = "my-es-topic"
}

```

### Input parameters
{: #event-streams-ds-input}

Review the input parameters that you can specify for your resource. 
{: shortdesc}

|Name|Data type|Required / optional|Description|
|----|-----------|-----------|---------------------|
|`resource_instance_id`|String|Required|The ID/CRN of the event streams service instance.|
|`name`|String|Required|The name of the topic.|
{: caption="Table. Available input parameters" caption-side="top"}

### Output parameters
{: #event-streams-ds-output}

Review the output parameters that you can access after your resource is created. 
{: shortdesc}

|Name|Data type|Description|
|----|-----------|--------|
|`id`|String|The ID of the topic in CRN format. For example, `crn:v1:bluemix:public:messagehub:us-south:a/6db1b0d0b5c54ee5c201552547febcd8:cb5a0252-8b8d-4390-b017-80b743d32839:topic:my-es-topic`|
|`kafka_http_url`|String|The API endpoint for interacting with event streams REST API.|
|`kafka_brokers_sasl`|Array of Strings|Kafka brokers use for interacting with Kafka native API.|
{: caption="Table 1. Available output parameters" caption-side="top"}
