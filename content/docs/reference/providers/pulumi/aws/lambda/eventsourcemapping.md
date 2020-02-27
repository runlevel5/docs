---
title: "EventSourceMapping"
---

<!-- WARNING: this file was generated by the Pulumi Terraform Bridge (tfgen) Tool. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

<style>
  table td p { margin-top: 0; margin-bottom: 0; }
</style>

Provides a Lambda event source mapping. This allows Lambda functions to get events from Kinesis, DynamoDB and SQS.

For information about Lambda and how to use it, see [What is AWS Lambda?][1].
For information about event source mappings, see [CreateEventSourceMapping][2] in the API docs.

> This content is derived from https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/r/lambda_event_source_mapping.html.markdown.


## Create a EventSourceMapping Resource

{{< langchoose csharp >}}

<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new</span> <span class="nx"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#EventSourceMapping>EventSourceMapping</a></span><span class="p">(</span><span class="nx">name</span>: <span class="kt"><a href=https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String>string</a></span><span class="p">,</span> <span class="nx">args</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#EventSourceMappingArgs>EventSourceMappingArgs</a></span><span class="p">,</span> <span class="nx">opts?</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions>pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>

```python
def __init__(__self__, resource_name, opts=None, batch_size=None, enabled=None, event_source_arn=None, function_name=None, maximum_batching_window_in_seconds=None, starting_position=None, starting_position_timestamp=None, __props__=None)
```

```go
func NewEventSourceMapping(ctx *pulumi.Context, name string, args *EventSourceMappingArgs, opts ...pulumi.ResourceOption) (*EventSourceMapping, error)

```

```csharp
public EventSourceMapping(string name, EventSourceMappingArgs args, CustomResourceOptions? options = null)

```

Creates a EventSourceMapping resource with the given unique name, arguments, and options.

{{% lang nodejs %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>args</strong> &ndash; (Required) The arguments to use to populate this resource's properties.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

{{% lang go %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>args</strong> &ndash; (Required) The arguments to use to populate this resource's properties.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

{{% lang csharp %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>args</strong> &ndash; (Required) The arguments to use to populate this resource's properties.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

The following arguments are supported:

<table class="ml-6">
    <thead>
        <tr>
            <th>Argument</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="align-top">batch<wbr>Size</td>
            <td class="align-top"><code>number</code></td>
            <td class="align-top">{{% md %}}
(Optional) The largest number of records that Lambda will retrieve from your event source at the time of invocation. Defaults to `100` for DynamoDB and Kinesis, `10` for SQS.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enabled</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
(Optional) Determines if the mapping will be enabled on creation. Defaults to `true`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">event<wbr>Source<wbr>Arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) The event source ARN - can be a Kinesis stream, DynamoDB stream, or SQS queue.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">function<wbr>Name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) The name or the ARN of the Lambda function that will be subscribing to events.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">maximum<wbr>Batching<wbr>Window<wbr>In<wbr>Seconds</td>
            <td class="align-top"><code>number</code></td>
            <td class="align-top">{{% md %}}
(Optional) The maximum amount of time to gather records before invoking the function, in seconds.  Records will continue to buffer until either `maximum_batching_window_in_seconds` expires or `batch_size` has been met. Defaults to as soon as records are available in the stream. If the batch it reads from the stream only has one record in it, Lambda only sends one record to the function.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">starting<wbr>Position</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The position in the stream where AWS Lambda should start reading. Must be one of `AT_TIMESTAMP` (Kinesis only), `LATEST` or `TRIM_HORIZON` if getting events from Kinesis or DynamoDB. Must not be provided if getting events from SQS. More information about these positions can be found in the [AWS DynamoDB Streams API Reference](https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_streams_GetShardIterator.html) and [AWS Kinesis API Reference](https://docs.aws.amazon.com/kinesis/latest/APIReference/API_GetShardIterator.html#Kinesis-GetShardIterator-request-ShardIteratorType).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">starting<wbr>Position<wbr>Timestamp</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) A timestamp in [RFC3339 format](https://tools.ietf.org/html/rfc3339#section-5.8) of the data record which to start reading when using `starting_position` set to `AT_TIMESTAMP`. If a record with this exact timestamp does not exist, the next later record is chosen. If the timestamp is older than the current trim horizon, the oldest available record is chosen.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## EventSourceMapping Output Properties

The following output properties are available:

<table class="ml-6">
    <thead>
        <tr>
            <th>Argument</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="align-top">batch<wbr>Size</td>
            <td class="align-top"><code>number</code></td>
            <td class="align-top">{{% md %}}
The largest number of records that Lambda will retrieve from your event source at the time of invocation. Defaults to `100` for DynamoDB and Kinesis, `10` for SQS.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enabled</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
Determines if the mapping will be enabled on creation. Defaults to `true`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">event<wbr>Source<wbr>Arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The event source ARN - can be a Kinesis stream, DynamoDB stream, or SQS queue.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">function<wbr>Arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The the ARN of the Lambda function the event source mapping is sending events to. (Note: this is a computed value that differs from `function_name` above.)

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">function<wbr>Name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The name or the ARN of the Lambda function that will be subscribing to events.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">last<wbr>Modified</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The date this resource was last modified.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">last<wbr>Processing<wbr>Result</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The result of the last AWS Lambda invocation of your Lambda function.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">maximum<wbr>Batching<wbr>Window<wbr>In<wbr>Seconds</td>
            <td class="align-top"><code>number</code></td>
            <td class="align-top">{{% md %}}
The maximum amount of time to gather records before invoking the function, in seconds.  Records will continue to buffer until either `maximum_batching_window_in_seconds` expires or `batch_size` has been met. Defaults to as soon as records are available in the stream. If the batch it reads from the stream only has one record in it, Lambda only sends one record to the function.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">starting<wbr>Position</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The position in the stream where AWS Lambda should start reading. Must be one of `AT_TIMESTAMP` (Kinesis only), `LATEST` or `TRIM_HORIZON` if getting events from Kinesis or DynamoDB. Must not be provided if getting events from SQS. More information about these positions can be found in the [AWS DynamoDB Streams API Reference](https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_streams_GetShardIterator.html) and [AWS Kinesis API Reference](https://docs.aws.amazon.com/kinesis/latest/APIReference/API_GetShardIterator.html#Kinesis-GetShardIterator-request-ShardIteratorType).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">starting<wbr>Position<wbr>Timestamp</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
A timestamp in [RFC3339 format](https://tools.ietf.org/html/rfc3339#section-5.8) of the data record which to start reading when using `starting_position` set to `AT_TIMESTAMP`. If a record with this exact timestamp does not exist, the next later record is chosen. If the timestamp is older than the current trim horizon, the oldest available record is chosen.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">state</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The state of the event source mapping.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">state<wbr>Transition<wbr>Reason</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The reason the event source mapping is in its current state.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">uuid</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The UUID of the created event source mapping.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Look up an Existing EventSourceMapping Resource

{{< langchoose csharp >}}

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: EventSourceMappingState, opts?: pulumi.CustomResourceOptions): EventSourceMapping;
```

```python
def get(resource_name, id, opts=None, acceleration_status=None, acl=None, arn=None, bucket=None, bucket_domain_name=None, bucket_prefix=None, bucket_regional_domain_name=None, cors_rules=None, force_destroy=None, hosted_zone_id=None, lifecycle_rules=None, loggings=None, object_lock_configuration=None, policy=None, region=None, replication_configuration=None, request_payer=None, server_side_encryption_configuration=None, tags=None, versioning=None, website=None, website_domain=None, website_endpoint=None)
```

```go
func GetBucket(ctx *pulumi.Context, name string, id pulumi.IDInput, state *BucketState, opts ...pulumi.ResourceOption) (*Bucket, error)
```

```csharp
public static Bucket Get(string name, Input<string> id, BucketState? state = null, CustomResourceOptions? options = null);
```

Get an existing EventSourceMapping resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

{{% lang nodejs %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>id</strong> &ndash; (Required) The _unique_ provider ID of the resource to lookup.</li>
    <li><strong>state</strong> &ndash; (Optional) Any extra arguments used during the lookup.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

{{% lang go %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>id</strong> &ndash; (Required) The _unique_ provider ID of the resource to lookup.</li>
    <li><strong>state</strong> &ndash; (Optional) Any extra arguments used during the lookup.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

{{% lang csharp %}}
<ul class="pl-10">
    <li><strong>name</strong> &ndash; (Required) The unique name of the resulting resource.</li>
    <li><strong>id</strong> &ndash; (Required) The _unique_ provider ID of the resource to lookup.</li>
    <li><strong>state</strong> &ndash; (Optional) Any extra arguments used during the lookup.</li>
    <li><strong>opts</strong> &ndash; (Optional) A bag of options that control this resource's behavior.</li>
</ul>
{{% /lang %}}

The following state arguments are supported:

<table class="ml-6">
    <thead>
        <tr>
            <th>Argument</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="align-top">batch<wbr>Size</td>
            <td class="align-top"><code>number</code></td>
            <td class="align-top">{{% md %}}
(Optional) The largest number of records that Lambda will retrieve from your event source at the time of invocation. Defaults to `100` for DynamoDB and Kinesis, `10` for SQS.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enabled</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
(Optional) Determines if the mapping will be enabled on creation. Defaults to `true`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">event<wbr>Source<wbr>Arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The event source ARN - can be a Kinesis stream, DynamoDB stream, or SQS queue.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">function<wbr>Arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The the ARN of the Lambda function the event source mapping is sending events to. (Note: this is a computed value that differs from `function_name` above.)

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">function<wbr>Name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The name or the ARN of the Lambda function that will be subscribing to events.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">last<wbr>Modified</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The date this resource was last modified.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">last<wbr>Processing<wbr>Result</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The result of the last AWS Lambda invocation of your Lambda function.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">maximum<wbr>Batching<wbr>Window<wbr>In<wbr>Seconds</td>
            <td class="align-top"><code>number</code></td>
            <td class="align-top">{{% md %}}
(Optional) The maximum amount of time to gather records before invoking the function, in seconds.  Records will continue to buffer until either `maximum_batching_window_in_seconds` expires or `batch_size` has been met. Defaults to as soon as records are available in the stream. If the batch it reads from the stream only has one record in it, Lambda only sends one record to the function.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">starting<wbr>Position</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The position in the stream where AWS Lambda should start reading. Must be one of `AT_TIMESTAMP` (Kinesis only), `LATEST` or `TRIM_HORIZON` if getting events from Kinesis or DynamoDB. Must not be provided if getting events from SQS. More information about these positions can be found in the [AWS DynamoDB Streams API Reference](https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_streams_GetShardIterator.html) and [AWS Kinesis API Reference](https://docs.aws.amazon.com/kinesis/latest/APIReference/API_GetShardIterator.html#Kinesis-GetShardIterator-request-ShardIteratorType).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">starting<wbr>Position<wbr>Timestamp</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) A timestamp in [RFC3339 format](https://tools.ietf.org/html/rfc3339#section-5.8) of the data record which to start reading when using `starting_position` set to `AT_TIMESTAMP`. If a record with this exact timestamp does not exist, the next later record is chosen. If the timestamp is older than the current trim horizon, the oldest available record is chosen.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">state</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The state of the event source mapping.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">state<wbr>Transition<wbr>Reason</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The reason the event source mapping is in its current state.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">uuid</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The UUID of the created event source mapping.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Import an Existing EventSourceMapping Resource

TODO

## Support Types
