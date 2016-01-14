title: How to setup Automatic Deployment of Hexo websites on Github Pages
date: 2016-01-14 13:20:00
tags:
  - hexo
  - automatic-deployment
  - github-pages
  - zammu
---


<link rel="stylesheet" type="text/css" href="/overrides.css" />
<link rel="stylesheet" type="text/css" href="/asciinema-player.css" />
<script src="/asciinema-player.js"></script>

[Hexo](https://hexo.io/) is a really powerful and fast static site generator. However, setting up Automatic Deployments for it is painful and tedious.

In this short post I'll show you how to get your Hexo website built on Github Pages automatically for each git push using [Zammu](https://zammu.in).

 1. Sign up for [zammu.in](https://zammu.in/hexo?invitation_code=HEXOAWESOME) using the invitation code `HEXOAWESOME`.
 2. Link up your Github Profile from zammu.in's home page after signing in.
 3. Create a new site using the "Github => Hexo => Github" recipe and enter the github url of your hexo website e.g. *zammu/hexo.zammu.in* with the other details.
 4. That's it. Now you whenever you push to your github repository, your website will be built using Hexo and will be published to Github Pages on subdomain.zammu.in

P.S I am the founder of [zammu](https://zammu.in/hexo?invitation_code=HEXOAWESOME) and would love to hear your feedback on it at [https://zammu.in/feedback](https://zammu.in/feedback?utm_src=hexo.zammu.in)

P.P.S This website is also hosted on [zammu](https://zammu.in/hexo). You can checkout its source at https://github.com/zammu/hexo.zammu.in

<div id="player-container"></div>
<script src='/load-player.js'></script>

- - -

**Here are the commands used in the above screencast if you want to copy them**

~~~bash
# init the new site
hexo init awesome-hexo-blog

# init the repo
cd awesome-hexo-blog
git init
git commit -m 'init'

# now we need to go to github and create our repository and then
git remote add origin git@github.com:minhajuddin/awesome-hexo-blog
git push origin master -u

# now we need to go to https://zammu.in/hexo and create a new site with the following  info
# Recipe = Github => Hexo => Github
# Title = My awesome Blog
# Domain =
# Subdomain = awesomehexo
# Github URL = minhajuddin/awesome-hexo-blog

echo "That's it we are done"
~~~
