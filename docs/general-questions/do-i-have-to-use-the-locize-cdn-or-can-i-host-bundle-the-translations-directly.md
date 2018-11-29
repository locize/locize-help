# Do I have to use the locize CDN or can i host / bundle the translations directly?

## Using our CDN or using custom solutions

While you get most comfort out of using our CDN your environment might demand you to bundle the translations with your product (eg. offline usage in areas with restricted internet access).

Using our **CDN** has three big **advantages**:

- You can deploy updates to translations without the need to redeploy/rollout a new version of your application.
- During development, testing you can set your versions to auto publishing. Doing so your translation changes are reflected immediately in your application and results in a lot easier development process.
- You can easily set a version to publish in private mode, which means you will need an API key to download your translations. This enables you for example to use locize as before but without leaking any information to the public.


## Download the translations

If your product demands to download the translations, because you need or prefer to host or bundle them yourself you can do so. Using our CDN is completely options and get only billed if you're using it.

Options to download the translations:

- Using our web applications
- Using the [API](https://docs.locize.com/api.html) or [locize-cli​](https://docs.locize.com/cli.html)

### Recommendation

We highly encourage you to at least use the CDN during development as it makes your work on translating your product a lot more efficient. Just bundle or change the i18next [backend implementation](https://www.i18next.com/plugins-and-utils.html#backends) during production.