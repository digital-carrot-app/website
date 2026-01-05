---
title: Capabilities
type: docs
weight: 100
# prev: /
# next: docs/folder/
---

Capabilities give plugins access to external resources such as the user's system and the internet. Think of capabilities as if they were library imports.

Capabilities are declared in the `imports` section of the `manifest.yaml`:

```yaml
imports:
  my_http_client:
    http_client:
      baseUrl: https://example.com
```

Usage in javascript:

```javascript
var out = my_http_client.get("/")
```

## Available Capbilities

{{< cards >}}
  {{< card link="http" title="Internet Access" subtitle="Access information from websites">}}
  <!--{{< card link="user_input" title="User Input" subtitle="Request input from the user" >}}-->
  {{< card link="oauth" title="Oauth2" subtitle="Login to websites and services via OAuth" >}}
  {{< card link="storage" title="Plugin Storage" subtitle="Store data on the user's account" >}}
{{< /cards >}}
