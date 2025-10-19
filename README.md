<!-- markdownlint-disable-next-line -->
<div align="center">

  <!-- markdownlint-disable-next-line -->
  # Personal Blog

  A minimal, responsive, and feature-rich Jekyll personal blog of a little bear :)

  <!-- TODO: Change this -->
  [**Live Demo**](https://tnhungct.github.io/)

  <!-- TODO: Change this -->
  ![](/assets/img/profile/screenshot.png)

</div>

## Prerequisite
- Ruby 3.4+
- Node 20+

## Add your new articles?

### Sidebar

If you want your page is attached to the sidebar (like CV page), put it in the `_tabs` folder.

### Changing avatar

Steps to change your avatar

- Go to page https://realfavicongenerator.net/
- Upload your avatar
- Download and unzip to folder `assets/imgs/favicons`
- Change `avatar` in `_config.yml`
- **Delete** folder `_site` if exists and **rebuild** your source. This is **important** to force page reload new icon.

### New article in collection

If you want to create a new article, put it in folder `_posts`. The article has this format `<year>-<month>-<date>-<title>.md`. It will create a nice timeline using the datetime information.

## How to build?

First you need to install all npm packages and build source to generate the minimal `js` files. Notes: the build require Nodejs 20+.

```bash
$ npm install
$ npm run build
```

After install, you will see it build something like theses on terminal:

```bash
[js] _javascript/commons.js → assets/js/dist/commons.min.js...
[js] created assets/js/dist/commons.min.js in 2.3s
[js] 
[js] _javascript/home.js → assets/js/dist/home.min.js...
[js] created assets/js/dist/home.min.js in 1.2s
[js] 
...
```

To build the static site using Jekyll, you need to install bundle, dependencies

```bash
$ bundle config set --local path 'vendor/bundle'
$ bundle install
```

Then build Jekyll and start the site

```bash
bundle exec jekyll build
bundle exec jekyll serve --watch
```
