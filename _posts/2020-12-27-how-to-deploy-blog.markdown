---
layout: post
title:  "How to Deploy Blog on Mac"
date:   2020-12-27 09:12:57 -0700
categories: jekyll update
---

I have followed [this blog][followed-blog] to deploy my blog on mac, but some problems were met. Thus, I write this blog to document the problems in case someone will meet the same ones.

## Problem 1
Everything is smooth until I performed this command `gem install jekyll bundler`, then I met the first error: 
{% highlight ruby %}
ERROR:  Error installing jekyll:
        ERROR: Failed to build gem native extension.
{% endhighlight %}
In order to solve this problem, you need to install `xcode`, but the command `xcode-select --install` did not work for me. I have to go to apple store and install `xcode` manually, and open it (to click 'agree'), then the problem solved.

## Problem 2
When I run `bundle exec jekyll serve`, I got this 

```
/home/argilo/.gem/ruby/3.0.0/gems/jekyll-4.2.0/lib/jekyll/commands/serve/servlet.rb:3:in `require': cannot load such file -- webrick (LoadError)
```

I followed [this][problem-2] instruction to solve this problem, the command you have to run is `bundle add webrick`. 

## Problem 3
Then I went through the remaining processes and see my page on web, but it is mess! The same problem as [this post][problem-3]. I followed the answer to modify the `baseurl` and `url` in file `_config.yml`:

```
baseurl: "/PengBlog" # the subpath of your site, e.g. /blog
url: "https://pzhao28.github.io" # the base hostname & protocol for your site, e.g. http://example.com
```

## Insert Image
Follow [this][insert-image]
![image](https://user-images.githubusercontent.com/41249426/103261509-118b6180-495f-11eb-88eb-779227a86782.png)


![image]({{ './images/config.png' | relative_url }}){: style="width: 600px; max-width: 100%;"}


Finally I got it! So you can see this blog. Woohoo!







[followed-blog]: https://medium.com/20percentwork/creating-your-blog-for-free-using-jekyll-github-pages-dba37272730a
[problem-2]: https://github.com/jekyll/jekyll/issues/8523
[problem-3]: https://github.com/cotes2020/jekyll-theme-chirpy/issues/63
[insert-image]: https://gist.github.com/kannankumar/4c613cac6d9db896062a16e1cc57d3e5