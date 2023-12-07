# Modifying this site

The site lives on a GitHub repository.

To update the site, you will need to pull this repository to your local computer either using the command line or an IDE (e.g., PyCharm).
From there, you need the `mkdocs` package to build and deploy the updated files to GitHub pages. All pages are written in Markdown, with hints of HTML here and there where needed.

1. Pull remote repository from GitHub

1. Make a change.

1. Commit the change.

1. Repeat the previous two steps until all changes are complete.

1. Push to remote repository on GitHub

1. From command prompt: `mkdocs build` to build the site locally 

1. From command prompt: `mkdocs gh-deploy` to publish the site to GitHub pages.