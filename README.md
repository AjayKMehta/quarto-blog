# Blog

[![Netlify Status](https://api.netlify.com/api/v1/badges/db14934e-1391-47d3-af07-18259a5ee7ed/deploy-status)](https://app.netlify.com/projects/ajaymehta/deploys)

This repository contains the source files for my [blog](https://ajaymehta.netlify.com/) built with [quarto](https://quarto.org/).

## Files

Here are some of the important files in this repository:

| File                | Description                |
|---------------------|----------------------------|
| _quarto.yml         | Quarto project file.       |
| index.qmd           | Blog home page.            |
| about.qmd           | Blog about page.           |
| posts/_metadata.yml | Shared options for posts   |
| styles.css          | Custom CSS for website     |
| LICENSE.md          | License info for website   |
| netlify.toml        | Configuration for Netlify  |

## Dependencies

- [Netlify CLI](https://docs.netlify.com/cli/get-started/)
- [Quarto CLI](https://quarto.org)

## Netlify CLI

For debugging output: `$env:DEBUG='*'`.

### Login

Login: `netlify login`. The access token will be stored in `~\AppData\Roaming\netlify\Config\config.json`

### Link to Netlify site

Run the following CLI command to link your local repository to your Netlify site:

```shell
neltlify link
```

### Build

```shell
netlify build
```

> :bulb: For local builds, the Netlify CLI will read the `.env` files you have stored in your local environment.

### Deploy

Deploy:

```shell
quarto render
netlify deploy
```

To customize the subdomain of your draft URL with a unique string, use the `--alias` flag with the `deploy` command.

```shell
netlify deploy --alias=draft
```

To deploy to production, add `--prod` (`-p`) flag.

### Run locally

```shell
netlify dev
```

## Publish using quarto

```shell
quarto publish netlify
```
