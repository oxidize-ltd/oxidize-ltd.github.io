# oxidize.cy

The website of Oxidize Ltd, served at [oxidize.cy](https://oxidize.cy) and built with
[Zola](https://www.getzola.org).

## Development

You need Zola 0.23 or later and [just](https://just.systems).

```shell
git clone --recurse-submodules git@github.com:oxidize-ltd/oxidize-ltd.github.io.git
just serve   # serve locally with live reload
just all     # check links and build into public/
```

## Design

The design comes from [tellus.rs](https://tellus.rs), included as the submodule `tellus-site`.
`sass/main.scss` imports its Sass partials and replaces the accent color; `static/fonts` is a
symlink to its fonts. To pick up changes to the tellus.rs design, run `just update-tellus-site`.

## Deployment

Every push to `main` is checked, built and deployed to GitHub Pages. Pull requests are only checked
and built. The custom domain comes from `static/CNAME`.
