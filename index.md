---
title: Home
layout: home
nav_order: 1
---

# About the template

This is a *bare-minimum* template to create a Jekyll site that uses the [Just the Docs] theme. You can easily set the created site to be published on [GitHub Pages] – the [README] file explains how to do that, along with other details.

If [Jekyll] is installed on your computer, you can also build and preview the created site *locally*. This lets you test changes before committing them, and avoids waiting for GitHub Pages.[^1] And you will be able to deploy your local build to a different platform than GitHub Pages.

More specifically, the created site:

- Uses a gem-based approach, i.e. uses a `Gemfile` and loads the `just-the-docs` gem
- Uses the [GitHub Pages / Actions workflow] to build and publish the site on GitHub Pages

Other than that, you're free to customize sites that you create with this template, however you like. You can easily change the versions of `just-the-docs` and Jekyll it uses, as well as adding further plugins.

[Browse our documentation][Just the Docs] to learn more about how to use this theme.

To get started with creating a site, simply:

1. Click "[use this template]" to create a GitHub repository
2. Go to Settings > Pages > Build and deployment > Source, and select GitHub Actions

If you want to maintain your docs in the `docs` directory of an existing project repo, see [Hosting your docs from an existing project repo](https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md#hosting-your-docs-from-an-existing-project-repo) in the template README.

# Building and previewing your site locally

Assuming [Jekyll][Jekyll Install] and Bundler are installed on your computer:

- Change your working directory to the root directory of your site.
- Run `bundle install`.
- Run `bundle exec jekyll serve` to build your site and preview it at `localhost:4000`.

The built site is stored in the directory `_site`.

# Publishing your site on GitHub Pages

1. If your created site is `YOUR-USERNAME/YOUR-SITE-NAME`, update `_config.yml` to:
    ```yaml
    title: YOUR TITLE
    description: YOUR DESCRIPTION
    theme: just-the-docs

    url: https://YOUR-USERNAME.github.io/YOUR-SITE-NAME

    # remove if you don't want this link to appear on your pages
    aux_links:
        Template Repository: https://github.com/YOUR-USERNAME/YOUR-SITE-NAME
    ```

2. Push your updated `_config.yml` to your site on GitHub.

3. In your newly created repo on GitHub:
    - Go to the Settings tab -> Pages -> Build and deployment, then select Source: GitHub Actions.
    - If there were any failed Actions, go to the Actions tab and click on Re-run jobs.

# Publishing your built site on a different platform

Just upload all the files in the directory `_site`.

----

[^1]: [It can take up to 10 minutes for changes to your site to publish after you push the changes to GitHub](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll#creating-your-site).

[Just the Docs]: https://just-the-docs.github.io/just-the-docs/
[GitHub Pages]: https://docs.github.com/en/pages
[README]: https://github.com/just-the-docs/just-the-docs-template/blob/main/README.md
[Jekyll]: https://jekyllrb.com
[GitHub Pages / Actions workflow]: https://github.blog/changelog/2022-07-27-github-pages-custom-github-actions-workflows-beta/
[use this template]: https://github.com/just-the-docs/just-the-docs-template/generate
[Jekyll Install]: https://idratherbewriting.com/documentation-theme-jekyll/mydoc_install_jekyll_on_mac.html#install-ruby-through-homebrew
