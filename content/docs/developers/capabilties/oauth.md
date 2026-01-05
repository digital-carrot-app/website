---
title: Oauth
type: docs
weight: 3
# prev: /
# next: docs/folder/
---
## Declaration

The oauth capability works a little bit differently. You declare it in imports just like any other capability, however instead of using it directly in your javascript,
you will instead reference it in your configuration schemas. In the example below, we're declaring an oauth login form field on the plugin's configuration schema using `metadata.oauth`. This instructs the app to handle the login redirect flow. 

```yaml
imports:
  my_oauth_client:
    oauth:
      # Client ID configured with the auth server
      client_id: my_id
      # Service specific scopes to request
      scopes:
        - scope1
      # Authorization url provided by the auth server
      auth_url: https://example.com/oauth/authorize
      # Token url provided by the auth server
      token_url: https://example.com/oauth/access_token
      # DO NOT USE THIS UNLESS REQUIRED BY THE AUTH SERVER. This secret is
      # not a secret! It has to be committed to the plugin repo.
      client_secret: my_secret
plugin_config_schema: plugin_config
schemas:
  plugin_config:
    type_input: object
    properties:
      login:
        metadata:
          oauth:
            oauth_instance: my_oauth_client
            service_name: Todoist
```

## Redirect URL

When the auth server asks for a redirect url use:

```
https://www.digitalcarrot.app/internal/oauth-callback/
```

## Example

This capability is used to authenticate the `http_client` object.

```javascript
function my_plugin_function(config, params){
  // pass the oauth schema field to the my_oauth_client.auth method to
  // generate credentials for an http client.
  my_http_client.setOauth(my_oauth_client.auth(config.login));

  my_http_client.get("/some/authenticated/api")
}
```
