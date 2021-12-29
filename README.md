# Webpage Privater Automarkt Radolfzell

You can find the sourcecode on [`https://github.com/michzuerch/Privater-Automarkt`](https://github.com/michzuerch/Privater-Automarkt);

## Working on this project

You need to install Node (tested with version 17.2.0) and npm.

### Format the code

```bash
# formating the code with prettier and eslint
npm run format
```

### Checking the code

```bash
# linting the code
npm run lint
```

### Testing

```bash
# running jest and cypress tests
npm run test
```

### Start the Dev-Environment

```bash
# formating the code with prettier and eslint
npm run dev

```

### Running a preview version

```bash
# formating the code with prettier and eslint
npm run preview
```

You can preview the built app with `npm run preview`, regardless of whether you installed an adapter. This should _not_ be used to serve your app in production.

### Create the productive build

```bash
# formating the code with prettier and eslint
npm run build
```

> The productive code to deploy is in the directory _public_

## CMS

To start directus run `npx directus start` in /directus. [Local Directus](http://localhost:8055)

---

## Todos

- Check /static/manifest.json on internet for docs.
- Integrate <https://rodneylab.com/sveltekit-seo> and <https://github.com/rodneylab/sveltekit-blog-mdx>
- Image processing <https://rodneylab.com/sveltekit-image-plugin>
- ImageDisplay.svelte hover animation
- Thumbnail.svelte transistion
