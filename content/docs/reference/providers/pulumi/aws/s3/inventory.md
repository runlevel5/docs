---
title: "Inventory"
---

<!-- WARNING: this file was generated by the Pulumi Terraform Bridge (tfgen) Tool. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

<style>
  table td p { margin-top: 0; margin-bottom: 0; }
</style>

Provides a S3 bucket [inventory configuration](https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-inventory.html) resource.

> This content is derived from https://github.com/terraform-providers/terraform-provider-aws/blob/master/website/docs/r/s3_bucket_inventory.html.markdown.


## Create a Inventory Resource

{{< langchoose csharp >}}

<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">new</span> <span class="nx"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#Inventory>Inventory</a></span><span class="p">(</span><span class="nx">name</span>: <span class="kt"><a href=https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String>string</a></span><span class="p">,</span> <span class="nx">args</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/aws/s3/#InventoryArgs>InventoryArgs</a></span><span class="p">,</span> <span class="nx">opts?</span>: <span class="kt"><a href=/docs/reference/pkg/nodejs/pulumi/pulumi/#CustomResourceOptions>pulumi.CustomResourceOptions</a></span><span class="p">);</span></code></pre></div>

```python
def __init__(__self__, resource_name, opts=None, bucket=None, destination=None, enabled=None, filter=None, included_object_versions=None, name=None, optional_fields=None, schedule=None, __props__=None)
```

```go
func NewInventory(ctx *pulumi.Context, name string, args *InventoryArgs, opts ...pulumi.ResourceOption) (*Inventory, error)

```

```csharp
public Inventory(string name, InventoryArgs args, CustomResourceOptions? options = null)

```

Creates a Inventory resource with the given unique name, arguments, and options.

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
            <td class="align-top">bucket</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) The S3 bucket configuration where inventory results are published (documented below).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">destination</td>
            <td class="align-top"><code><a href="#inventorydestination">Inventory<wbr>Destination</a></code></td>
            <td class="align-top">{{% md %}}
(Required) Contains information about where to publish the inventory results (documented below).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enabled</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies whether the inventory is enabled or disabled.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">filter</td>
            <td class="align-top"><code><a href="#inventoryfilter">Inventory<wbr>Filter</a></code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies an inventory filter. The inventory only includes objects that meet the filter's criteria (documented below).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">included<wbr>Object<wbr>Versions</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) Object versions to include in the inventory list. Valid values: `All`, `Current`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) Unique identifier of the inventory configuration for the bucket.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">optional<wbr>Fields</td>
            <td class="align-top"><code>Array&lt;<wbr>string<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) List of optional fields that are included in the inventory results.
Valid values: `Size`, `LastModifiedDate`, `StorageClass`, `ETag`, `IsMultipartUploaded`, `ReplicationStatus`, `EncryptionStatus`, `ObjectLockRetainUntilDate`, `ObjectLockMode`, `ObjectLockLegalHoldStatus`, `IntelligentTieringAccessTier`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">schedule</td>
            <td class="align-top"><code><a href="#inventoryschedule">Inventory<wbr>Schedule</a></code></td>
            <td class="align-top">{{% md %}}
(Required) Specifies the schedule for generating inventory results (documented below).

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Inventory Output Properties

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
            <td class="align-top">bucket</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
The S3 bucket configuration where inventory results are published (documented below).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">destination</td>
            <td class="align-top"><code><a href="#inventorydestination">Inventory<wbr>Destination</a></code></td>
            <td class="align-top">{{% md %}}
Contains information about where to publish the inventory results (documented below).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enabled</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
Specifies whether the inventory is enabled or disabled.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">filter</td>
            <td class="align-top"><code><a href="#inventoryfilter">Inventory<wbr>Filter</a></code></td>
            <td class="align-top">{{% md %}}
Specifies an inventory filter. The inventory only includes objects that meet the filter's criteria (documented below).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">included<wbr>Object<wbr>Versions</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
Object versions to include in the inventory list. Valid values: `All`, `Current`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
Unique identifier of the inventory configuration for the bucket.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">optional<wbr>Fields</td>
            <td class="align-top"><code>Array&lt;<wbr>string<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
List of optional fields that are included in the inventory results.
Valid values: `Size`, `LastModifiedDate`, `StorageClass`, `ETag`, `IsMultipartUploaded`, `ReplicationStatus`, `EncryptionStatus`, `ObjectLockRetainUntilDate`, `ObjectLockMode`, `ObjectLockLegalHoldStatus`, `IntelligentTieringAccessTier`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">schedule</td>
            <td class="align-top"><code><a href="#inventoryschedule">Inventory<wbr>Schedule</a></code></td>
            <td class="align-top">{{% md %}}
Specifies the schedule for generating inventory results (documented below).

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Look up an Existing Inventory Resource

{{< langchoose csharp >}}

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: InventoryState, opts?: pulumi.CustomResourceOptions): Inventory;
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

Get an existing Inventory resource's state with the given name, ID, and optional extra
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
            <td class="align-top">bucket</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The S3 bucket configuration where inventory results are published (documented below).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">destination</td>
            <td class="align-top"><code><a href="#inventorydestination">Inventory<wbr>Destination</a></code></td>
            <td class="align-top">{{% md %}}
(Optional) Contains information about where to publish the inventory results (documented below).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">enabled</td>
            <td class="align-top"><code>boolean</code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies whether the inventory is enabled or disabled.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">filter</td>
            <td class="align-top"><code><a href="#inventoryfilter">Inventory<wbr>Filter</a></code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies an inventory filter. The inventory only includes objects that meet the filter's criteria (documented below).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">included<wbr>Object<wbr>Versions</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) Object versions to include in the inventory list. Valid values: `All`, `Current`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">name</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) Unique identifier of the inventory configuration for the bucket.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">optional<wbr>Fields</td>
            <td class="align-top"><code>Array&lt;<wbr>string<wbr>&gt;</code></td>
            <td class="align-top">{{% md %}}
(Optional) List of optional fields that are included in the inventory results.
Valid values: `Size`, `LastModifiedDate`, `StorageClass`, `ETag`, `IsMultipartUploaded`, `ReplicationStatus`, `EncryptionStatus`, `ObjectLockRetainUntilDate`, `ObjectLockMode`, `ObjectLockLegalHoldStatus`, `IntelligentTieringAccessTier`.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">schedule</td>
            <td class="align-top"><code><a href="#inventoryschedule">Inventory<wbr>Schedule</a></code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies the schedule for generating inventory results (documented below).

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

## Import an Existing Inventory Resource

TODO

## Support Types

#### InventoryDestination

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
            <td class="align-top">bucket</td>
            <td class="align-top"><code><a href="#inventorydestinationbucket">Inventory<wbr>Destination<wbr>Bucket</a></code></td>
            <td class="align-top">{{% md %}}
(Required) The S3 bucket configuration where inventory results are published (documented below).

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

#### InventoryDestinationBucket

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
            <td class="align-top">account<wbr>Id</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The ID of the account that owns the destination bucket. Recommended to be set to prevent problems if the destination bucket ownership changes.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">bucket<wbr>Arn</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) The Amazon S3 bucket ARN of the destination.

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">encryption</td>
            <td class="align-top"><code><a href="#inventorydestinationbucketencryption">Inventory<wbr>Destination<wbr>Bucket<wbr>Encryption</a></code></td>
            <td class="align-top">{{% md %}}
(Optional) Contains the type of server-side encryption to use to encrypt the inventory (documented below).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">format</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) Specifies the output format of the inventory results. Can be `CSV`, [`ORC`](https://orc.apache.org/) or [`Parquet`](https://parquet.apache.org/).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">prefix</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The prefix that is prepended to all inventory results.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

#### InventoryDestinationBucketEncryption

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
            <td class="align-top">sse<wbr>Kms</td>
            <td class="align-top"><code><a href="#inventorydestinationbucketencryptionssekms">Inventory<wbr>Destination<wbr>Bucket<wbr>Encryption<wbr>Sse<wbr>Kms</a></code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies to use server-side encryption with AWS KMS-managed keys to encrypt the inventory file (documented below).

{{% /md %}}</td>
        </tr>
        <tr>
            <td class="align-top">sse<wbr>S3</td>
            <td class="align-top"><code><a href="#inventorydestinationbucketencryptionsses3">Inventory<wbr>Destination<wbr>Bucket<wbr>Encryption<wbr>Sse<wbr>S3</a></code></td>
            <td class="align-top">{{% md %}}
(Optional) Specifies to use server-side encryption with Amazon S3-managed keys (SSE-S3) to encrypt the inventory file.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

#### InventoryDestinationBucketEncryptionSseKms

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
            <td class="align-top">key<wbr>Id</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) The ARN of the KMS customer master key (CMK) used to encrypt the inventory file.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

#### InventoryDestinationBucketEncryptionSseS3

#### InventoryFilter

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
            <td class="align-top">prefix</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Optional) The prefix that is prepended to all inventory results.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>

#### InventorySchedule

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
            <td class="align-top">frequency</td>
            <td class="align-top"><code>string</code></td>
            <td class="align-top">{{% md %}}
(Required) Specifies how frequently inventory results are produced. Valid values: `Daily`, `Weekly`.

{{% /md %}}</td>
        </tr>
    </tbody>
</table>
