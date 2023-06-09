---
title: "Documentation"
lead: "This page will explain how to contribute to this documentation"
weight: 5030
toc: true
---

## Getting started

For contributing you will need the following:

- git installed, this will most likely already be the case
- a GitHub account
- a text or markdown editor like VSCode
- some knowledge of markdown ([guide to markdown](https://www.markdownguide.org/basic-syntax))
- nodejs is also strongly recommended, especially when creating new pages to see how changes appear on the wiki

To set up your editing environment you will need to fork and clone the [repository](https://github.com/an-anime-team/docs). The following will show you how to create your own copy (fork) and download (clone) it.

Open the repository in a browser, log in to GitHub and click on "Fork" in the top right. Just click on "Create fork" in the next step and you will have forked the repository!

To clone your fork type `git clone https://github.com/[your GitHub username]/docs.git` into a terminal and git will create a directory named docs and download the repository there.

Now you just need to edit something!

## Previewing edits

The recommended way to preview changes is to start a local instance of the website. Before the first launch you will need to install the dependencies: run `npm install` in the directory of the docs. Starting the local server is done by running `npm run start`, now you can open [localhost:1313](http://localhost:1313) in your browser to view the wiki. Just save your files and the website will automatically be updated to reflect your changes.

## Uploading your edits

After you are done with your edits you will need to commit your changes with `git commit -m 'I changed something'` and push your changes with `git push`. If you are prompted for your GitHub credentials you will most likely need to create an [access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token#creating-a-personal-access-token-classic).

Next open your repository, click on "Contribute" and open a pull request.

## Code of conduct

- Date format: [ISO](https://greenwichmeantime.com/articles/clocks/iso)
