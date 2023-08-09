# NuxtJS Jam Stack Style Portfolio Site
## Introduction
My personal portfolio site, built with Vue.js (Nuxt.js) and Bulma, hosted on Netlify.
[![Netlify Status](https://api.netlify.com/api/v1/badges/254ea0ea-e33d-42d5-a2ad-cd6e0928be2e/deploy-status)](https://app.netlify.com/sites/competent-jang-7cd087/deploys)

## Progress of project
Basic skeleton with HTML content finished.
Mobile Friendly nav menu finished.
Nuxt Content implemented, but this is a limited use case, it lets me use Markdown files as 'content management' but as it currently stands it is only 1 step above hard-coding everything anyway. I'll have to look at the implementation a bit more. One of the touted powers of using Nuxt Content as a 'headless CMS' is being able to use Markdown files to simulate a Git-based CMS. But right now I can't make changes to the MD files unless I push to repo anyway, so what is the difference?

## Planned changes
- UX features like smooth scrolling, hover/focus effects, and more color and pop.
- Overhaul overall design, create and implement mockups. Need a light and dark mode as part of the redesign.
- Overhaul style sheet implementation, I really need a proper system here and not just throwing down CSS code when I need something to look a certain way, maybe think about a more formal component building system
- Continuing exploring Nuxt Content and CMS like functionality.

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).
