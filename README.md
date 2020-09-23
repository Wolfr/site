# Svelte Society Site

This repository contains the source code for the Svelte Society website. It is comprised of a couple of different pieces that are important to understand when contributing.

Technologies used:
* Routify
* MDSveX
* Cloudflare Worker Site

## Contributing

Find an issue worth pursuing and pull down the repo. Run `npm install` followed by `npm run dev:nollup`. You can now access the site at `localhost:8080`.

If you want to expand the site or do larger work, such as adding new sections to the site, please come to the [Discord](https://discord.gg/JcvNM8p) and discuss it with us first. Otherwise you might be doing work that won't get merged and that's not fun for anyone!

## Recipes

The recipes are written and processed using [Mdsvex](https://mdsvex.com/). Three helper components are provided, located in `src/components/recipes` that can be used to highlight certain parts of a recipe.

- **Warning** Can be used to inform a reader of common pitfall or point to take extra care
- **Note** To highlight something noteworthy
- **ReadMore** Use this to wrap extra reading material related to the recipe

**⚠️ Be aware that markdown inside of these components will not be processed, so when putting for instance a link inside use normal HTML markup to do so. ⚠️**

### Example usage

```md
---
title: Sample
---

<script>
  import ReadMore from '../../../components/recipes/ReadMore.svelte'
  import Warning from '../../../components/recipes/Warning.svelte'
</script>

This is regular text

<Warning>
    This is text within the block
</Warning>

<ReadMore>
  Click <a href="/">here</a> to read more about this.
</ReadMore>
```
