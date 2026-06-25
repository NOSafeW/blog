# NoSafeW Blog

Hugo source for the NoSafeW blog at:

- https://blog.nosafew.com/

## Development

```sh
hugo server
```

## Build

```sh
hugo --gc --minify
```

The generated `public/` directory is ignored locally. GitHub Actions builds and
deploys the site to GitHub Pages.

