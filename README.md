# strapi-provider-upload-bunnycdn

BunnyCDN Upload Provider for Strapi

## Configurations

See the [using a provider](https://strapi.io/documentation/developer-docs/latest/development/plugins/upload.html#using-a-provider) documentation for information on installing and using a provider. And see the [environment variables](https://strapi.io/documentation/developer-docs/latest/setup-deployment-guides/configurations.html#environment-variables) for setting and using environment variables in your configs.

**Example**

`./config/plugins.js`

```js
module.exports = ({ env }) => ({
  //...
  upload: {
    provider: 'bunnycdn',
    providerOptions: {
      region: env('BUNNYCDN_HOST'),
      apiKey: env('BUNNYCDN_API_KEY'),
      storageZone: env('BUNNYCDN_STORAGE_ZONE'),
      pullZone: env('BUNNYCDN_PULL_ZONE')
    },
  },
  //...
});
```

`.env`

```
BUNNYCDN_HOST: Storage primary Hostname (Inside FTP & API Access).
BUNNYCDN_API_KEY: Storage Password (Inside FTP & API Access).
BUNNYCDN_STORAGE_ZONE: Storage Zone name.
BUNNYCDN_PULL_ZONE: Pull Zone name.
```