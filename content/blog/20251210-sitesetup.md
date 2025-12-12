+++
title = "Site Setup"
date = "2025-12-10"
description = "A recap of how I set the site up"

[taxonomies]
tags = ["zola", "tabi", "cicd", "todo"]
+++

## The process

Setting this site up went quite smoothly. There were a couple of points of confusion but they were resolved and I've got a clean site to record the things I will learn.

### Technology choices

I had previously found [Zola](https://www.getzola.org/), a Static Site Generator built in [Rust](https://rust-lang.org/). I went through the the [Getting stated guide](https://www.getzola.org/documentation/getting-started/overview/) and explored the [Themes](https://www.getzola.org/themes/).

I found the [tabi theme](https://github.com/welpo/tabi) which has a lot of functionality and is regularly maintained. While it would be interesting to make my own theme and start from scratch, this would take a lot of time away from recording my learning.

There was an unsuccessful attempt to apply the tabi theme over my code from the Getting Started Guide. This is most likely due to not copying all the required files over, or removing multi-lingual files which I didn't need.

#### Actions

- I made a new repo from the [tabi-start](https://github.com/welpo/tabi-start) template and was able to make progress.
- Adding the theme repo as a submodule,
- Updating the config file
- and drafting my first blog post.

### Deployment confusion

The next step was to upload the site to Github pages. There was some confusion with the workflow, as I saw multiple code snippets with different environmental variables and I had overlooked the guidance to grant additional permissions to the worker via the GitHub website. I focused on the error message that mentioned the repo giving 403 errors and associcated it with the config option to insert a link to the repo, rather than the core deployment.

#### Actions

- I used the [Zola Deploy Action](https://github.com/shalzz/zola-deploy-action), it had the right ENV value
- I noticed updated the permissions for the worker from the repo settings.

### Domain setup

I had previously set up my domain as a custom domain with Github so I'm a bit hazy on the authentication approach, a TXT record IIRC.

#### Actions

- For this site, I needed to add the intended domain to a CNAME file in the website root (put it in the static directory and it's moved in the build)
- Then I updated DNS to point to it.

### Git

Due to my config confusion, I had some unwanted commits. While I knew I could remove the commits from history and force push, it was safer to just revert the commits that I didn't need. I tried removing both in a single commit but this didn't work so there were 2 commits that I then rebased into a single commit.

## Future Learning

- Customise the theme: I'm not too fond of the current accent colour, how can I change this in a way that won't break updates from upstream?
- Site architecture: I now have 2 blog pages. The start repo also has an archive and projects section. How best to use these?
- Any new functionality: What else can tabi do? Are there any new features I'd want to implement?
- Learn more about Github workflows: I was able to get it working by following some instructions and the files are quite readable. Are there any new flows I'd want to implement?
- Use git more and document it: I wasn't confident on the syntax for reverting and rebasing, or the notations for describing commits. Being able to use this without searching will be helpful.
- Content workflow: I'm currently drafting on main, how should I write future articles? One branch per article, or a draft branch? I'll go for a branch per article. Will test it now.
- Formalise review steps
