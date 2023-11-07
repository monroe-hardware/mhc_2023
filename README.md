# MHC Web Site

This repository contains the source and build files for the Monroe Hardware Company website.

## How This Works

This site uses Grunt and the Trilliant static site builder. The source code for the builder is located in `src/builder` while the Grunt tasks for the builder and test server are defined in `src/grunt`. The test server runs locally via `trilliant-webserver`.


The template files are all contained in the `tmpl` directory while all pages are defined in the `content` directory. These are all assembled via Grunt into a static site in the `www` directory. The `deploy` task will deploy this site to the `gh-pages` branch of this repo to be served on GitHub.


## Deploy

```
grunt deploy --target=live
```

The above command will build all scripts and pages, using the `live` configuration, then commit the contents of the `www` directory to the `gh-pages` branch for publication.

## Test Server

```
grunt test
```

By default, the command above will build all scripts and pages, copy assets, and launch a local web server on port `8889` to view and test the site.

