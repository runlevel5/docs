---
title: "ConfigurationTemplate"
---

<!-- WARNING: this file was generated by the Pulumi Terraform Bridge (tfgen) Tool. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

<style>
  table td p { margin-top: 0; margin-bottom: 0; }
</style>

Provides an Elastic Beanstalk Configuration Template, which are associated with
a specific application and are used to deploy different versions of the
application with the same configuration settings.

## Option Settings

The `setting` field supports the following format:

* `namespace` - unique namespace identifying the option's associated AWS resource
* `name` - name of the configuration option
* `value` - value for the configuration option
* `resource` - (Optional) resource name for [scheduled action](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/command-options-general.html#command-options-general-autoscalingscheduledaction)

> This content is derived from https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/r/elastic_beanstalk_configuration_template.html.markdown.


## Create a ConfigurationTemplate Resource

{{< langchoose csharp >}}

<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new</span> <span class="nx"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#ConfigurationTemplate>ConfigurationTemplate</a></span><span class="p">(</span><span class="nx">name</span>: <span class="kt"><a href=https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String>string</a></span><span class="p">,</span> <span class="nx">args</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#ConfigurationTemplateArgs>ConfigurationTemplateArgs</a></span><span class="p">,</span> <span class="nx">opts?</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions>pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>

```python
def __init__(__self__, resource_name, opts=None, application=None, description=None, environment_id=None, name=None, settings=None, solution_stack_name=None, __props__=None)
```

```go
func NewConfigurationTemplate(ctx *pulumi.Context, name string, args *ConfigurationTemplateArgs, opts ...pulumi.ResourceOption) (*ConfigurationTemplate, error)

```

```csharp
public ConfigurationTemplate(string name, ConfigurationTemplateArgs args, CustomResourceOptions? options = null)

```

Creates a ConfigurationTemplate resource with the given unique name, arguments, and options.

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
            <td class="align-top">application</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) name of the application to associate with this configuration template

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">description</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) Short description of the Template

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">environment<wbr>Id</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The ID of the environment used with this configuration template

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) A unique name for this Template.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">settings</td>
            <td class="align-top"><code>Array&lt;<wbr><a href="#configurationtemplatesetting">Configuration<wbr>Template<wbr>Setting</a><wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) Option settings to configure the new Environment. These
override specific values that are set as defaults. The format is detailed
below in Option Settings

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">solution<wbr>Stack<wbr>Name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) A solution stack to base your Template
off of. Example stacks can be found in the [Amazon API documentation][1]

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## ConfigurationTemplate Output Properties

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
            <td class="align-top">application</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
name of the application to associate with this configuration template

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">description</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
Short description of the Template

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">environment<wbr>Id</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The ID of the environment used with this configuration template

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
A unique name for this Template.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">settings</td>
            <td class="align-top"><code>Array&lt;<wbr><a href="#configurationtemplatesetting">Configuration<wbr>Template<wbr>Setting</a><wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
Option settings to configure the new Environment. These
override specific values that are set as defaults. The format is detailed
below in Option Settings

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">solution<wbr>Stack<wbr>Name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
A solution stack to base your Template
off of. Example stacks can be found in the [Amazon API documentation][1]

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Look up an Existing ConfigurationTemplate Resource

{{< langchoose csharp >}}

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: ConfigurationTemplateState, opts?: pulumi.CustomResourceOptions): ConfigurationTemplate;
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

Get an existing ConfigurationTemplate resource's state with the given name, ID, and optional extra
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
            <td class="align-top">application</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) name of the application to associate with this configuration template

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">description</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) Short description of the Template

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">environment<wbr>Id</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The ID of the environment used with this configuration template

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) A unique name for this Template.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">settings</td>
            <td class="align-top"><code>Array&lt;<wbr><a href="#configurationtemplatesetting">Configuration<wbr>Template<wbr>Setting</a><wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) Option settings to configure the new Environment. These
override specific values that are set as defaults. The format is detailed
below in Option Settings

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">solution<wbr>Stack<wbr>Name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) A solution stack to base your Template
off of. Example stacks can be found in the [Amazon API documentation][1]

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Import an Existing ConfigurationTemplate Resource

TODO

## Support Types

#### ConfigurationTemplateSetting

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
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) A unique name for this Template.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">namespace</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) 
{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">resource</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) 
{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">value</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) 
{{% /md %}}</td>
        </tr>
    </tbody>
</table>
