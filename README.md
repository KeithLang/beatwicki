# Beat Wicki website preview

Static preview of the Wicki Informations- und Kommunikationsrecht site, deployed to Cloudflare Pages at https://beatwicki.pages.dev/.

The `preview/` folder is the deploy root: `index.html` is a self-contained build exported from the design project, and `_headers` sets noindex.

Deploy:

```
npx wrangler pages deploy preview --project-name beatwicki --branch main
```

## Video variant (not deployed)

`preview-video/` holds a second version of the same site. The five Rechtsgebiete are cards, and each card plays a short looping clip on hover. On phones the clip plays while the card is on screen.

The folder is a deploy root of its own: `index.html`, `_headers` (noindex) and `video/`, which holds five MP4 clips and their poster images. The clips load only when first played and total 2.1 MB.

This variant has not been deployed anywhere. The client link above still serves `preview/`. To put the variant on a separate preview address without touching that link:

```
npx wrangler pages deploy preview-video --project-name beatwicki --branch video
```

Cloudflare then serves it at https://video.beatwicki.pages.dev/. To make it the client-facing site instead, deploy `preview-video` with `--branch main`.

The editable source is the page "Wicki Kundenvorschau Video" in the Wicki design project.
