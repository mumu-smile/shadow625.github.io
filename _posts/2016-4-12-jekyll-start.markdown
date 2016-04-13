---
layout: post
title: jekyll——安装过程及界面定制
subtitle: "Jekyll——road"
author: "Shadow"
avatar: "image/IMG_2916.jpg"
thumbnail: fa-anchor
date:   2016-4-12 12:12:12
---


用jekyll好久了（好吧一直是通过github-page简介用的）今天终于在自己的电脑上搭好了Jekyll的本地环境（你问我装了多长时间： 6个月你信不信）在这里记录下Jekyll的搭建和使用的一些经验吧
首先我是在github—pages 上第一次接触Jekyll 
当时正想搭建一个博客平台，但是感觉wordpress太low（应该就是了解不深导致印象不好吧），自己写前段改代码又太菜，这时实验室同桌在搞的一个博客界面吸引了我的眼球，界面很清新，功能不多不少，正是我脑海中完美的一个博客环境，（对，没错 我就是那个时候才知道有github-pages这个东西）而且有很多漂亮的开源模板可以使用（不信是吧，来看看[Jekyll主题](http://jekyllthemes.org/))

##安装Jekyll##

* github主页就是通过Jekyll渲染的，也就是说在他的后台肯定是配备了一个Jekyll环境，我们现在就是试图在本地搭建一个一模一样的环境，用于本地测试。当然你要是一片markdown错误率能保持在0以下，那么这环境就是多余的了。（想想应该不可能呢，因为你还有耐心在看这篇文，说明我们俩水平差不多吧）
	根据[Jekyll官网](https://jekyllrb.com/)给的简单的示例，
    <pre><code>  $ gem install jekyll</br>
    $ jekyll new my-awesome-site
    $ cd my-awesome-site
    $ jekyll serve</code></pre>
*然而事实并没有那么简单在我执行第一步的时候就卡住了，Mac是自带Ruby的，我就直接输入命令泡好茶等结果，然后发现他一直执行不出来，然后就开始查（此处省略好多字）
![no_response](/image/gem_no_response.png)
最后知道，需要执行gem update --system （什么鬼，感觉就像yum的更新源吧）然后执行Jekyll安装就顺利了。（还是没有反应的话借个梯子试试）
后面的事情就很轻松了，如果这个时候你在上面选好了你的界面模板，那就git clone过来，在模板根目录下直接`Jekyll serve`就可以在本地访问你的准博客界面了。
##界面定制
这个我并不是前端专家，但是模板都有了，做一些改动的话还是很轻松的嘛。
如果你有过django开发经历处理这个就太简单了。他们两个之间的差异很小，上手很容易。现在来介绍一下他的目录结构
    <pre><code calss="nohighlight">.
    |── _config.yml
	|── _drafts
    |   |── begin-with-the-crazy-ideas.textile
	|   |── on-simplicity-in-technology.markdown
	|── _includes
	|   |── footer.html
	|   |── header.html
	|── _layouts
	|   |── default.html
	|   |── post.html
	|── _posts
	|   |── 2007-10-29-why-every-programmer-should-play-nethack.textile
	|   |── 2009-04-26-barcamp-boston-4-roundup.textile
	|── _site
	|── .jekyll-metadata
	|── index.html
</code></pre>
