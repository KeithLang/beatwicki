# Beat Wicki website preview

Static preview of the Wicki Informations- und Kommunikationsrecht site, deployed to Cloudflare Pages at https://beatwicki.pages.dev/.

The `preview/` folder is the deploy root: `index.html` is a self-contained build exported from the design project, and `_headers` sets noindex.

Deploy:

```
npx wrangler pages deploy preview --project-name beatwicki --branch main
```
