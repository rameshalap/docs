page_main_title: Docker Datacenter (Deprecated)
main_section: Platform
sub_section: Integrations
sub_sub_section: Deprecated
page_title: Docker Datacenter integration (Deprecated)

# Docker Datacenter Integration (Deprecated)

## Deprecation Note
This integration has been deprecated. A new integration called [Docker Datacenter](/platform/integration/ddcKey) of generic type has been introduced which can be used instead.

If you have any existing Docker Datacenter integrations of type deploy, you can continue to use them.

---

The **Docker Datacenter** Integration is used to connect Shippable DevOps Assembly Lines platform to Docker Datacenter so that you can deploy Docker based applications.

## Creating an Integration

Since this integration has been deprecated, you cannot create new integrations for this, you can only edit/delete the existing Docker Datacenter integrations. You can use the new [Docker Datacenter](/platform/integration/ddcKey) of type generic instead.

## Usage in Assembly Lines

The Docker Datacenter integration can be used in the following [resources](/platform/workflow/resource/overview/):

* [cluster](/platform/workflow/resource/cluster)
* [integration](/platform/workflow/resource/integration)

### Default Environment Variables
When you create a resource with this integration, and use it as an `IN` or `OUT` for a `runSh` or `runCI` job, a set of environment variables is automatically made available that you can use in your scripts.

`<NAME>` is the the friendly name of the resource with all letters capitalized and all characters that are not letters, numbers or underscores removed. Any numbers at the beginning of the name are also removed to create a valid variable. For example, `my-key-1` will be converted to `MYKEY1`, and `my_key_1` will be converted to `MY_KEY_1`.

| Environment variable						| Description                         |
| ------------- 								|------------------------------------ |
| `<NAME>`\_INTEGRATION\_USERNAME   		| Username supplied in the integration |
| `<NAME>`\_INTEGRATION\_PASSWORD			| Password supplied in the integration |
| `<NAME>`\_INTEGRATION\_URL				| URL supplied in the integration |

### Shippable Utility Functions
To make it easy to use these environment variables, the platform provides a command line utility that can be used to work with these values.

How to use these utility functions is [documented here](/platform/tutorial/workflow/using-shipctl).

## Further Reading
* [Quick Start to CI](/getting-started/ci-sample)
* [RunSh Job](/platform/workflow/job/runsh)
* [Jobs](/platform/workflow/job/overview)
* [Resources](/platform/workflow/resource/overview)
