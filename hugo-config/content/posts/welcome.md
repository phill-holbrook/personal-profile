+++ 
draft = false
date = 2022-04-10T22:04:38-04:00
title = "Welcome!"
description = ""
slug = ""
authors = []
tags = []
categories = []
externalLink = ""
series = []
+++

## Welcome!

This is my first blog post for my personal website. I was recently introduced to [Hugo](https://gohugo.io/) by a colleague and decided to spin this site up as a weekend project. I already had a free tier AWS EC2 instance running my [Dog Facts](https://github.com/phill-holbrook/dog-facts) Discord bot, and I had already implemented a [CI/CD pipeline](https://github.com/phill-holbrook/dog-facts/blob/master/.github/workflows/main.yml) for that project (using GitHub Actions and AWS CodeDeploy to automatically deploy the bot to the EC2 whenever I pushed code changes to GitHub).

With that framework already in place, getting this site up and running was really easy. I followed the [Quick Start](https://gohugo.io/getting-started/quick-start/) guide to install Hugo on my WSL2 system, and after some testing and getting used to it, decided to use the [Coder](https://github.com/luizdepra/hugo-coder) theme. Initially I ran into a lot of trouble getting it to work, but it was because I did not heed the warnings about not using apt:

>This option is not recommended because the Hugo in Linux package managers for Debian and Ubuntu is usually a few versions behind as described [here](https://github.com/gcushen/hugo-academic/issues/703).

I removed that package and grabbed the latest version of Hugo from the official release page [here](https://github.com/gohugoio/hugo/releases). After installing that, I was able to successfully test the Coder theme using Coder's quick start guide. Then, I came across [this fantastic guide aimed for Hugo beginners](https://acanalis.github.io/post/concepts-of-hugo/) by @acanalis. I followed the steps from section 2.2 of that guide to merge the Coder theme with my Hugo site and I was off to the races (after [a traditional manual install of GoLang, of course](https://go.dev/doc/install)).

From there, I installed Apache and CertBot in my EC2 instance, set up the appropriate security group rules to allow inbound 80 and 443 to the instance, and copied my Dog Facts pipeline in with a few modifications, and it's looking good! Another successful weekend project under the belt. 
