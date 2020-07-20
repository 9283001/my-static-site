---
layout: post
title: UAT and PROD
date: 2020-07-19
author: the Finn
---
## How to serve CSS locally and on production

When you build the site on localhost:4000 use

	bundle exec jekyll serve --baseurl ''

Config.yml has baseurl: "my-static-site" which is needed to properly render the css on PROD.

On localhost:4000, `--baseurl ''` passes an empty string, so it skips directly to `/assets/main.css` even though base url is set as “my-static-site”.