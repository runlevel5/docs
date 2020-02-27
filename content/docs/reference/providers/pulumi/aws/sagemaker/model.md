---
title: "Model"
---

<!-- WARNING: this file was generated by the Pulumi Terraform Bridge (tfgen) Tool. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

<style>
  table td p { margin-top: 0; margin-bottom: 0; }
</style>

Provides a SageMaker model resource.

> This content is derived from https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/r/sagemaker_model.html.markdown.


## Create a Model Resource

{{< langchoose csharp >}}

<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new</span> <span class="nx"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#Model>Model</a></span><span class="p">(</span><span class="nx">name</span>: <span class="kt"><a href=https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String>string</a></span><span class="p">,</span> <span class="nx">args</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#ModelArgs>ModelArgs</a></span><span class="p">,</span> <span class="nx">opts?</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions>pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>

```python
def __init__(__self__, resource_name, opts=None, containers=None, enable_network_isolation=None, execution_role_arn=None, name=None, primary_container=None, tags=None, vpc_config=None, __props__=None)
```

```go
func NewModel(ctx *pulumi.Context, name string, args *ModelArgs, opts ...pulumi.ResourceOption) (*Model, error)

```

```csharp
public Model(string name, ModelArgs args, CustomResourceOptions? options = null)

```

Creates a Model resource with the given unique name, arguments, and options.

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
            <td class="align-top">containers</td>
            <td class="align-top"><code>Array&lt;<wbr><a href="#modelcontainer">Model<wbr>Container</a><wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies containers in the inference pipeline. If not specified, the `primary_container` argument is required. Fields are documented below.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enable<wbr>Network<wbr>Isolation</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
(Optional) Isolates the model container. No inbound or outbound network calls can be made to or from the model container.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">execution<wbr>Role<wbr>Arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) A role that SageMaker can assume to access model artifacts and docker images for deployment.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The name of the model (must be unique). If omitted, this provider will assign a random, unique name.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">primary<wbr>Container</td>
            <td class="align-top"><code><a href="#modelprimarycontainer">Model<wbr>Primary<wbr>Container</a></code></td>
            <td class="align-top">{{% md %}}
(Optional) The primary docker image containing inference code that is used when the model is deployed for predictions.  If not specified, the `container` argument is required. Fields are documented below.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">tags</td>
            <td class="align-top"><code>Map&lt;<wbr>any<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) A mapping of tags to assign to the resource.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">vpc<wbr>Config</td>
            <td class="align-top"><code><a href="#modelvpcconfig">Model<wbr>Vpc<wbr>Config</a></code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies the VPC that you want your model to connect to. VpcConfig is used in hosting services and in batch transform.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Model Output Properties

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
            <td class="align-top">arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The Amazon Resource Name (ARN) assigned by AWS to this model.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">containers</td>
            <td class="align-top"><code>Array&lt;<wbr><a href="#modelcontainer">Model<wbr>Container</a><wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
Specifies containers in the inference pipeline. If not specified, the `primary_container` argument is required. Fields are documented below.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enable<wbr>Network<wbr>Isolation</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
Isolates the model container. No inbound or outbound network calls can be made to or from the model container.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">execution<wbr>Role<wbr>Arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
A role that SageMaker can assume to access model artifacts and docker images for deployment.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The name of the model (must be unique). If omitted, this provider will assign a random, unique name.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">primary<wbr>Container</td>
            <td class="align-top"><code><a href="#modelprimarycontainer">Model<wbr>Primary<wbr>Container</a></code></td>
            <td class="align-top">{{% md %}}
The primary docker image containing inference code that is used when the model is deployed for predictions.  If not specified, the `container` argument is required. Fields are documented below.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">tags</td>
            <td class="align-top"><code>Map&lt;<wbr>any<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
A mapping of tags to assign to the resource.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">vpc<wbr>Config</td>
            <td class="align-top"><code><a href="#modelvpcconfig">Model<wbr>Vpc<wbr>Config</a></code></td>
            <td class="align-top">{{% md %}}
Specifies the VPC that you want your model to connect to. VpcConfig is used in hosting services and in batch transform.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Look up an Existing Model Resource

{{< langchoose csharp >}}

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: ModelState, opts?: pulumi.CustomResourceOptions): Model;
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

Get an existing Model resource's state with the given name, ID, and optional extra
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
            <td class="align-top">arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The Amazon Resource Name (ARN) assigned by AWS to this model.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">containers</td>
            <td class="align-top"><code>Array&lt;<wbr><a href="#modelcontainer">Model<wbr>Container</a><wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies containers in the inference pipeline. If not specified, the `primary_container` argument is required. Fields are documented below.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enable<wbr>Network<wbr>Isolation</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
(Optional) Isolates the model container. No inbound or outbound network calls can be made to or from the model container.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">execution<wbr>Role<wbr>Arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) A role that SageMaker can assume to access model artifacts and docker images for deployment.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The name of the model (must be unique). If omitted, this provider will assign a random, unique name.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">primary<wbr>Container</td>
            <td class="align-top"><code><a href="#modelprimarycontainer">Model<wbr>Primary<wbr>Container</a></code></td>
            <td class="align-top">{{% md %}}
(Optional) The primary docker image containing inference code that is used when the model is deployed for predictions.  If not specified, the `container` argument is required. Fields are documented below.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">tags</td>
            <td class="align-top"><code>Map&lt;<wbr>any<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) A mapping of tags to assign to the resource.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">vpc<wbr>Config</td>
            <td class="align-top"><code><a href="#modelvpcconfig">Model<wbr>Vpc<wbr>Config</a></code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies the VPC that you want your model to connect to. VpcConfig is used in hosting services and in batch transform.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Import an Existing Model Resource

TODO

## Support Types

#### ModelContainer

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
            <td class="align-top">container<wbr>Hostname</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) 
{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">environment</td>
            <td class="align-top"><code>Map&lt;<wbr>any<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) 
{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">image</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) 
{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">model<wbr>Data<wbr>Url</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) 
{{% /md %}}</td>
        </tr>
    </tbody>
</table>

#### ModelPrimaryContainer

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
            <td class="align-top">container<wbr>Hostname</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) 
{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">environment</td>
            <td class="align-top"><code>Map&lt;<wbr>any<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) 
{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">image</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) 
{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">model<wbr>Data<wbr>Url</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) 
{{% /md %}}</td>
        </tr>
    </tbody>
</table>

#### ModelVpcConfig

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
            <td class="align-top">security<wbr>Group<wbr>Ids</td>
            <td class="align-top"><code>Array&lt;<wbr>string<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Required) 
{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">subnets</td>
            <td class="align-top"><code>Array&lt;<wbr>string<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Required) 
{{% /md %}}</td>
        </tr>
    </tbody>
</table>
