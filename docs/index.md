---
layout: ""
page_title: "Provider: Looker"
description: |-
  The Looker provider provides resources to interact with a Looker instance API.
---

# Looker Provider

The Looker provider provides resources to interact with a Looker instance API.

To use the Looker provider, you will need API credentials. These can be generated at `https://org.cloud.looker.com/admin/users` and come in the form of "API3 Keys": <abbr title="\b[a-zA-Z0-9]{20}\b">`client_id`</abbr> and <abbr title="\b[a-zA-Z0-9]{24}\b">`client_secret`</abbr>.
Ensure the user used as owner of the API keys has sufficient admin permissions.


## Example Usage

```terraform
terraform {
  required_providers {
    looker = {
      source  = "devoteamgcloud/looker"
      version = "0.1.2"
    }
  }
}

provider "looker" {
  base_url      = "https://org.cloud.looker.com:19999/api/" # Optionally use env var LOOKER_BASE_URL
  client_id     = "12345678"                                # Optionally use env var LOOKER_API_CLIENT_ID
  client_secret = "abcd1234"                                # Optionally use env var LOOKER_API_CLIENT_SECRET
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `base_url` (String) For base_url, provide the URL including /api/ ! Normally, a REST API should not have api in it's path, therefore we don't add the /api/ inside the provider.
- `client_id` (String)
- `client_secret` (String, Sensitive)