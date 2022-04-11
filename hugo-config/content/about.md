---
title: "About Me"
date: 2022-04-10T21:52:52-04:00
draft: false
---
Hi! I'm Phill. I'm an experienced IT professional interested in automation, scripting, and DevOps. I built this site to demonstrate skills I've learned through home labbing and independent study, inspired by the [Cloud Resume Challenge](https://cloudresumechallenge.dev/docs/the-challenge/aws/). This is actually Version 2 of the site. For Version 1, [see here](https://phill.holbrook.cc/). Version 2 is built using [Hugo](https://gohugo.io/).

Version 1 has a visitor counter at the top of the page uses JavaScript to call (via AWS API Gateway) a [Python script](https://github.com/phill-holbrook/resume_back-end/blob/master/visitor-counter/app.py) that runs in AWS Lambda. The script reads from and updates a DynamoDB table to keep track of how many visitors I've had on the site. Implementing this feature in Version 2 is currently on the To Do list.

I've also implemented [a small CI/CD pipeline using GitHub Actions](https://github.com/phill-holbrook/personal-profile/actions/workflows/main.yml) which publish updates to this site whenever I push to GitHub. In Version 2, I'm using GitHub Actions to interact with AWS CodeDeploy to copy the hugo-config folder to a location on my EC2 instance, then run a set of deployment scripts which builds the site, reloads Apache, and verifies Apache is running. In [Version 1](https://github.com/phill-holbrook/resume_front-end), this was much easier since that site is a single page of HTML stored as a static file in S3. I did have to make sure to invalidate CloudFront cache, though, so the published updates are visible instantly.

My GitHub profile also has some of my other side projects, including the first version of this site (built manually with HTML and CSS), a Slack bot that provides cat facts, a Discord bot that provides dog facts, and some Python projects while going through A Cloud Guru's Intro to Python Development course.

If you have any questions feel free to reach out to me via email or on LinkedIn!
