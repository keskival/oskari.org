# Oskari.org map application framework's web site

## Installation

```
// clone the repository
cd oskari.org
npm install
node app
```

Additionally, if you want the `.less` and `.js` files to be compiled to and linked from `/public`, run `gulp` in the main directory.

## Structure

Documentation and guides are in `md` directory as `markdown` documents. After creating a new document remember to reference it from either a page in `views/documentation.jade` or `views/guides.jade` (or another appropriate place) or from another document.

When added under `md/documentation` or `md/guides` the page is automatically routed to `/documentation/<file location without the md extension>` or `/guides/<file location without the md extension>`, respectively.

All the other content should be placed in the `.jade` templates under `views/`. Also, please see the `routes.js` for details on how the content gets rendered.

See the KaPa interface specification in [md/documentation/bundles/statistics/kapa.md](md/documentation/bundles/statistics/kapa.md).
