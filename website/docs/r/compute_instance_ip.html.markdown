---
layout: "scaleway"
page_title: "Scaleway: scaleway_compute_instance_ip"
description: |-
  Manages Scaleway Compute Instance IPs.
---

# scaleway_compute_instance_ip

Creates and manages Scaleway Compute Instance IPs. For more information, see [the documentation](https://developers.scaleway.com/en/products/instance/api/#ips-268151).

## Example Usage

```hcl
resource "scaleway_compute_instance_ip" "server_ip" {}
```

## Arguments Reference

The following arguments are supported:

- `reverse` - (Optional) The reverse DNS for this IP.
- `server_id` - (Optional) The ID of the server you want to attach this resource to.
- `zone` - (Defaults to [provider](../index.html#zone) `zone`) The [zone](../guides/regions_and_zones.html#zones) in which the IP should be reserved.
- `project_id` - (Defaults to [provider](../index.html#project_id) `project_id`) The ID of the project the IP is associated with.

## Attributes Reference

In addition to all arguments above, the following attributes are exported:

- `id` - The ID of the IP.
- `address` - The IP address.

## Import

IPs can be imported using the `{zone}/{id}`, e.g.

```bash
$ terraform import scaleway_compute_instance_ip.server_ip fr-par-1/11111111-1111-1111-1111-111111111111
```
