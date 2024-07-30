# Website for DevOps KC

DevOps KC is a community for DevOps practitioners and tech enthusiasts in Kansas City and surrounding areas.

<img src="/assets/images/logo.png" alt="devops kc logo" width="300">

## Contributing

### Setup

1. Make sure you have [Hugo installed](https://gohugo.io/installation/)
2. [Fork the repo](https://github.com/DevOpsKC/website/fork), and then clone the repo locally (ideally into a directory like `devopskc-website` so you know what's what) along with the theme as a submodule:

***Note: the site uses the theme as a Hugo Module, and uses it on build. Using the `--recursive` flag will bring in the theme so you can easily see what's happening. Don't make any changes to the files in the theme folder though.***

```bash
git clone --recursive <forked repo url> devopskc-website
cd devopskc-website
```

3. Install / Update the NPM dependencies:

```bash
npm install
```

4. Verify you can see the site by starting the Hugo dev server:

```bash
hugo server
```

4. The site should now be on http://localhost:1313

***Note: to make sure you have the latest version of the theme for dev purposes, you can run the following to update the theme: `git submodule update --remote --merge`***

### File structure

The site is built with Hugo, and the theme is in the `/themes/hugoplate` folder once you have cloned the repo. Otherwise, check the [theme source](https://github.com/zeon-studio/hugoplate).

- The base site's config is in `hugo.toml`, for base info like URL, title, etc.
- The full [configuration](https://gohugo.io/getting-started/configuration/) is in the `config` folder, separated out by the following folders:
  - `_default` for the site's default configuration which applies to everything
    - `languages.toml` for the site's languages
    - `menus.en.toml` for the site's english menus
    - `module.toml` for the site's module config, like imports
    - `params.toml` for the site's parameters, like sections, logos, etc. See Hugo config for more info
  - `development` for config that only applies to development, i.e. local
  - `production` for config that only applies to production, i.e. the live site
- The site's assets that get built when the site builds (logos, scss, custom css, etc.) are in the `assets` directory.
- The site's modified (from the theme) and any custom layouts are in the `layouts` directory.
- The site's content is in the `content` directory, organized by section and/or pages:
  - `about` folder for the site's about page, with the content in the residing `_index.md` file
  - `contact` folder for the site's contact page, with the content in the residing `_index.md` file
  - `pages` folder for the site's other pages, if applicable, with a file for each page
  - `sections` folder for the different sections of the site, with a file for each section
  - `_index.md` for the site's home page content
- Any content that doesn't need compiled, i.e. doesn't change, should go into the `static` directory.
- The `data` folder contains data files that are used by the site.
- The `themes` folder contains the theme files. ***DO NOT EDIT THESE FILES***

For more info on Hugo's directory structure, see [Hugo's docs](https://gohugo.io/getting-started/directory-structure/).

## Credits

- Site framework: [Hugo Static site generator](https://gohugo.io), minumum version 0.130.x
- Theme: [Hugoplate](https://github.com/zeon-studio/hugoplate) by Zeon Studio
- 
