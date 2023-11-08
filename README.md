<h1 align="center">
  <a href="https://www.svix.com">
    <img width="120" src="https://avatars.githubusercontent.com/u/80175132?s=200&v=4" />
    <p align="center">Svix - Webhooks as a service</p>
  </a>
</h1>

# Upload Event Types to Svix - GitHub Action

This GitHub action reads and uploads an OpenAPI spec (in JSON or YAML) format and uploads it to Svix to create event types for your webhooks.
For more information, check out [our docs](https://docs.svix.com/event-types#upload-openapi-specification).

## Inputs

### `openapi-file`

**Required**  
Location of the OpenAPI spec file (can be in JSON or YAML format).

### `svix-api-key`

**Required**  
Your [Svix API key](https://docs.svix.com/api-keys). 

### `svix-api-url`

**Optional**
Override the Svix API URL. If not set, the URL will be determined using the API Key.

## Usage

To use this GitHub Action in your workflow, you can add the following step:

```yaml
- name: Upload Event Types to Svix
  uses: svix/svix-event-type-import-action@v1
  with:
    openapi-file: 'path/to/your/openapi-spec.yml'
    svix-api-key: ${{ secrets.SVIX_API_KEY }}
```

## Documentation

For a more information, checkout our [API reference](https://docs.svix.com).
