---
page_title: "looker_user Resource - terraform-provider-looker"
subcategory: ""
description: |-
  
---
# looker_user (Resource)

## Example Usage
```terraform
resource "looker_user" "user_a" {
  first_name = "Xavier"
  last_name  = "Waterslaeghers"
  email      = "xavier.w@ipv4.plus"
}
```

## Example Output
```terraform
# looker_user.user_a:
resource "looker_user" "user_a" {
    id         = "167"
    email      = "xavier.w@ipv4.plus"
    first_name = "Xavier"
    last_name  = "Waterslaeghers"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `already_exists_ok` (Boolean) Set to true if the user already exists and you want to use it. If user doesn't exist, it will be created.
- `delete_on_destroy` (Boolean) Set to false if you want the user to not be deleted on destroy plan.
- `email` (String)
- `first_name` (String)
- `last_name` (String)
- `roles` (Set of String)

### Read-Only

- `id` (String) The ID of this resource.
- `last_updated` (String)
