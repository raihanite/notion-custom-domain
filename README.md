# Notion Custom Domain

Custom domains for your Notion pages. You can publish your page to your own domain instead of `notion.site`.

[![Notion Custom Domain](https://user-images.githubusercontent.com/19500280/93695277-d99aa400-fb4f-11ea-8e82-5c431110ce19.png)](https://notion-custom-domain.hosso.co)

## Getting Started

Install dependencies:

```
yarn
```

Then deploy to Vercel with specifying your public Notion page:

```
PAGE_URL=https://<your-domain>.notion.site/<Your-Page-ID> \
yarn deploy:prod
```

For example:

```
PAGE_URL=https://notion.notion.site/Notion-Official-83715d7703ee4b8699b5e659a4712dd8 \
yarn deploy:prod
```

Finally, set up a custom domain for the deployment on the Vercel Dashboard. See [Custom Domains – Vercel Docs](https://vercel.com/docs/concepts/projects/custom-domains)

![](https://user-images.githubusercontent.com/19500280/169642461-c31df143-a8a5-4d37-8494-e5b04b01c7b1.png)

## Development

### Run locally

```
PAGE_URL=https://<your-domain>.notion.site/<Your-Page-ID> \
yarn dev
```

Then open http://localhost:3000.

### Debug with Node Inspector

```
PAGE_URL=https://<your-domain>.notion.site/<Your-Page-ID> \
yarn debug
```

Then open http://localhost:3000.

## Google Analytics Support

Deploying with `GA_MEASUREMENT_ID` environment variable injects the tracking code into your public Notion page:

```
PAGE_URL=https://<your-domain>.notion.site/<Your-Page-ID> \
GA_MEASUREMENT_ID=G-XXXXXXXXXX \
yarn deploy:prod
```

## Using Environment Variables on the Vercel Dashboard

You can use environment variables on the Vercel Dashboard. In this case, you can simply run
`vercel env pull`, `vercel dev`, `vercel deploy` or `vercel deploy --prod` without setting environment variables.
![](https://github.com/hosso/notion-custom-domain/assets/19500280/e234a2eb-8ba7-4be0-a1dd-fa58ce0327ab)

## License

[MIT](LICENSE)
