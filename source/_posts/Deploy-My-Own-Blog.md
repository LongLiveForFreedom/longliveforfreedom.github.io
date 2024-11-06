---
title: Deploy My Own Blog
date: 2024-11-06 13:39:36
tags:
---
# Deploy my own blog with hexo(theme: Shoka) and github
## Prepare
- a github account
- install Git(get ssh working) and Nodejs on your PC or Mac
## Hexo
- install
`sudo npm install -g hexo-cli`
without sudo may encounter permission issues result in install fail
- init your blog folder
`hexo init blog`
`cd blog`
![](./Deploy-My-Own-Blog/Screenshot%202024-11-06%20at%2014.09.59.png)
- install some dependencies
`sudo npm install`
`sudo npm install hexo-deployer-git --save`
- get writing root for blog file
`sudo chmod -R 777 blog`
- preview your blog
`hexo s`
visit http://localhost:4000/ you will see your blog page
- (optional) download a theme from https://hexo.io/themes/ and move the file to /blog/themes
- the Shoka theme is here https://github.com/amehime/hexo-theme-shoka
## Github pages
- create a repository namely username.github.io
- modify the deploy section in /root/_config.yml
```shell
deploy:
  type: git
  repo: https://github.com/username/username.github.io.git
  branch: main
```
- after coding your blog, you can deploy it
`hexo g`
`hexo d`
- visit http://username.github.io then you will see your blog
## Create a new blog
`hexo new "new blog name"`
put the picture in file with the same name of the new blog