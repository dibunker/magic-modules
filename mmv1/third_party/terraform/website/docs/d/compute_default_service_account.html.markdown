---
subcategory: "Compute Engine"
description: |-
  Retrieve default service account used by VMs running in this project
---

# google_compute_default_service_account

Use this data source to retrieve default service account for this project

## Example Usage

```hcl
data "google_compute_default_service_account" "default" {
}

output "default_account" {
  value = data.google_compute_default_service_account.default.email
}
```

## Argument Reference

The following arguments are supported:

* `project` - (Optional) The project ID. If it is not provided, the provider project is used.


## Attributes Reference

The following attributes are exported:

* `email` - Email address of the default service account used by VMs running in this project

* `unique_id` - The unique id of the service account.

* `name` - The fully-qualified name of the service account.

* `display_name` - The display name for the service account.

* `member` - The Identity of the service account in the form `serviceAccount:{email}`. This value is often used to refer to the service account in order to grant IAM permissions.
