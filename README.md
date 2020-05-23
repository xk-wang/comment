# Comment

​     Comment is a place to store the comments of my blog produced by gitalk. My blog page is https://xk-wang.github.io/blog/, and my homepage  https://xk-wang.github.io is still under construction. If you are intersted in these, you are welcome to give me the issue and fork me in Github.

​     Here I'd like to introduce the main technologies used in my blog and some funny story about this blog. More deitails can be seen in my blog https://xk-wang.github.io/blog/.

## Technologies

- jekyll

  > ​    Jekyll is a static site generator. General website construction needs the combination of front-end and back-end. This often involves HTML, CSS, JS, database and other knowledge. The time cost of building a site from scratch is often high. 
  >
  > ​    Static site generator provides a easy way to do a good job in some aspects, such as personal blog. This kind of site often has the characteristics of small visit and relatively fixed content. Static site genertator can provide a better respond speed in this situation.
  >
  > ​    Jekyll is one of static site generators, which makes focus more on content creation. By using html, css and js, we can design the style and behavior of our sites. All the rest we need do is just to write markdown !
  >
  >    The technology of Jekyll can be learn from https://jekyllrb.com/ .

- gitalk

  > ​     Gitalk is a comment plug-in. With a few lines of code in the front end, we can provide our site the comment funtion. Gitalk and gitment are both comment plug-ins, and they are almost the same. Gitalk and gitment use github issue to store the comments of our sites, so there is no need to use database anymore. 
  >
  > ​     The combination of jekyll and gitalk can be learned from  https://aerolith.ink/2018/08/25/Gitalk/.

  

- github pages

  > Buying a host and domain name costs money and requires a series of configurations. Github pages provides free personal domain and certain storage space for us to place static sites. How to use github pages can be learned from https://help.github.com/en/github/working-with-github-pages. 

## Some stories

This is the first time I use jekyll to set up my blog site. It cost about two days to finish. In this process, I met three problems and final solved them.

- Jekyll and github page gem dependency. 

  ​    In the website of github pages https://help.github.com/en/github/working-with-github-pages, it doesn't talk much about this important issue. To install jekyll, I have to install Ruby installer first. I installed the latest Ruby installer. However, I couldn't start my jekyll site no matter what I did. The key is that I should install jekyll 3.8.5, so the Ruby installer version can't be to high. The detail dependency can be see from https://pages.github.com/versions/.

- Create the blog style of my own.

  ​    Writing the style for my own blog is not easy because I am not familiar with css. Although github pages provide some themes, them don't look good. So finally I decide to find a template from http://jekyllthemes.org/.

- Be familiar with jekyll config file.

  ​    Indeed, a bug about this take me one day to solve it. It is the github username (site.github.username) in _config.yml files. I don't know why jekyll reads it in js files as null. As a result, I can't visite my comment repository correctly and get a 404 Error in my gitalk. Finally I solved it using site.gitalk.admin value as an alternative.