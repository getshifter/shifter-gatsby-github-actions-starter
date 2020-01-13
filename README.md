# shifter-gatsby-github-actions

Example Gatsby site using WordPress and WPGraphQL hosted on Shifter, builds using GitHub Actions, and deploys to Netlify.

## This Repo Explained

### Gatsby

This repo is an example Gatsby site. You can use it as a starter or pull just what you need. It's based on [Jason Bahl's WPGraphQL starter](https://github.com/wp-graphql/gatsby-wpgraphql-blog-example).

### Shifter

The WordPress source site is hosted on [Shifter](https://www.getshifter.io). Shifter is a static site generator for WordPress and the backend starts and stops as needed. In this case we are using it to host the content for Gatsby because we only need WordPress to start during builds and stop after they are complete. Starting and stopping WordPress reduces the number of attack vectors and Shifter can also create a static site from your existing WordPress theme. Sourcing static assets for Gatsby can be done by using the static site Shifter creates if you are not downloading files during your Gatsby build.

### GitHub Actions

Inside .github/workflows/main.yml, located in this project you'll find the config file for GitHub Actions. These actions cover the Gatsby build process on each push to master.

### Netlify

The static site created by Gatsby is hosted on Netlify. After the build is creating using GitHub Actions, those files are deployed to Netlify.

