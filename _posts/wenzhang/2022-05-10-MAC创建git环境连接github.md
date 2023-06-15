---
layout: post
title: "MAC搭建jekll环境连接Github Blog"
author: zhangsan
subtitle: Each post also has a subtitle
categories: wenzhang
tags: [test]
---

主要介绍如何在MAC从无到有安装Git和Jekyll环境，以及下载上传代码到github上.  <img src="/images/龙猫.jpeg" width="20%">  

![测试图](/images/龙猫.jpeg)
## 1.Github上创建仓库  

## 2.MAC上搭建jekyll环境  

### （1）安装Git
```js
brew install git
```
### （2）安装ruby
```js
brew install chruby ruby-install
ruby-install ruby
echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
echo "chruby ruby-3.1.1" >> ~/.zshrc 
// 这里的ruby版本根据实际安装的版本来
然后只需ruby -v 验证即可
```
### （3）安装jekyll
```markdown
gem install jekyll  bundler
```
### （4）本地启动jekyll环境
本地启动jekyll环境后，即可根据提示打开https://127.0.0.1:4000打开博客进行预览，方便调试页面，等确认完全后发布到Github上。
```makrdown
❯ jekyll serve --trace
## 遇到第3点中错误时采用该命令执行
❯ bundle exec jekyll serve --trace
```
## 3.MAC启动jekyll环境的错误解决方法
```markdown
// 报错提示信息1：
❯ jekyll serve --trace                                                                                                                      ─╯
/Users/moyu/.gem/ruby/3.1.2/gems/bundler-2.3.13/lib/bundler/runtime.rb:309:in `check_for_activated_spec!': You have already activated mercenary 0.4.0, but your Gemfile requires mercenary 0.3.6. Prepending `bundle exec` to your command may solve this. (Gem::LoadError)
	from /Users/moyu/.gem/ruby/3.1.2/gems/bundler-2.3.13/lib/bundler/runtime.rb:25:in `block in setup'
---
	from /Users/moyu/.gem/ruby/3.1.2/gems/bundler-2.3.13/lib/bundler/spec_set.rb:136:in `each'
	from /Users/moyu/.gem/ruby/3.1.2/gems/bundler-2.3.13/lib/bundler/spec_set.rb:136:in `each'
	from /Users/moyu/.gem/ruby/3.1.2/gems/jekyll-4.2.2/exe/jekyll:11:in `<top (required)>'
	from /Users/moyu/.gem/ruby/3.1.2/bin/jekyll:25:in `load'
	from /Users/moyu/.gem/ruby/3.1.2/bin/jekyll:25:in `<main>'
// 解决方法：
❯ bundle exec jekyll serve --trace  

// 报错提示信息2：
❯ bundle exec jekyll serve --trace                                                                                                          ─╯
Configuration file: /Users/moyu/Documents/owner/GitHub/blog/slurm/_config.yml
            Source: /Users/moyu/Documents/owner/GitHub/blog/slurm
       Destination: /Users/moyu/Documents/owner/GitHub/blog/slurm/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
  Dependency Error: Yikes! It looks like you don't have kramdown-parser-gfm or one of its dependencies installed. In order to use Jekyll as currently configured, you'll need to install this gem. The full error message from Ruby is: 'cannot load such file -- kramdown-parser-gfm' If you run into trouble, you can find helpful resources at https://jekyllrb.com/help/!
  Conversion error: Jekyll::Converters::Markdown encountered an error while converting '_posts/2017-04-20-my-example-post.md':
                    kramdown-parser-gfm
             ERROR: YOUR SITE COULD NOT BE BUILT:
                    ------------------------------------
                    kramdown-parser-gfm
// 解决方法：
❯ gem install kramdown-parser-gfm  ##确认已经安装时可忽略
❯ bundle add kramdown-parser-gfm

// 报错提示信息3：
❯ bundle exec jekyll serve --trace                                                                                                          ─╯
Configuration file: /Users/moyu/Documents/owner/GitHub/blog/slurm/_config.yml
            Source: /Users/moyu/Documents/owner/GitHub/blog/slurm
       Destination: /Users/moyu/Documents/owner/GitHub/blog/slurm/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 0.867 seconds.
 Auto-regeneration: enabled for '/Users/moyu/Documents/owner/GitHub/blog/slurm'
bundler: failed to load command: jekyll (/Users/moyu/.gem/ruby/3.1.2/bin/jekyll)
/Users/moyu/.gem/ruby/3.1.2/gems/jekyll-3.9.2/lib/jekyll/commands/serve/servlet.rb:3:in `require': cannot load such file -- webrick (LoadError)
	from /Users/moyu/.gem/ruby/3.1.2/gems/jekyll-3.9.2/lib/jekyll/commands/serve/servlet.rb:3:in `<top (required)>'
	from /Users/moyu/.gem/ruby/3.1.2/gems/jekyll-3.9.2/lib/jekyll/commands/serve.rb:184:in `setup'
	from /Users/moyu/.gem/ruby/3.1.2/gems/jekyll-3.9.2/lib/jekyll/commands/serve.rb:102:in `process'
	from /Users/moyu/.gem/ruby/3.1.2/gems/jekyll-3.9.2/lib/jekyll/commands/serve.rb:93:in `block in start'
// 解决方法：
❯ bundle add webrick
```
# [](#header-1)Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## [](#header-2)Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### [](#header-3)Header 3

```

```ruby
# Ruby code with syntax highlighting
GitHubPages::Dependencies.gems.each do |gem, version|
  s.add_dependency(gem, "= #{version}")
end
```

#### [](#header-4)Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### [](#header-5)Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### [](#header-6)Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
