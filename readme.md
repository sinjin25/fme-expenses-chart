# Overview
Front End Mentor project creating and implementing from a supplied design doc.

# Live Site
https://sinjin25.github.io/fme-expenses-chart/

# Getting the Vue site to work on GH pages
1. remove `dist` from `.gitignore`
2. Github repo: settings > pages > github actions
3. Select "deploy static content"
4. In the generated `.yml` file, change `with: path: '.'` to `with: path: './dist`
5. Follow this guide for creating a subtree https://learnvue.co/tutorials/deploy-vue-to-github-pages#step-3-run-git-add-dist--git-commit--m-adding-dist-subtree (I did not write this)