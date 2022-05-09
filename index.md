## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/moyu5021/slurm/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdow
拥有仓库写入权限的人员可以使用 Jekyll 向 GitHub Pages 站点添加内容。
必须先创建一个 Jekyll 站点，然后才可将内容添加到 GitHub Pages 上的 Jekyll 站点。 
使用 Jekyll 创建 GitHub Pages 站点”：
1.安装ruby
          brew install chruby ruby-install
          ruby-install ruby
          echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
          echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
          echo "chruby ruby-3.1.1" >> ~/.zshrc （这里的ruby版本根据实际安装的版本来）
          然后只需ruby -v 验证即可
2.安装Jekyll
          gem install jekyll  bundler
3.安装git
          brew install git
4.使用jekyll构建一个默认的站点myblog出来
          jekyll new myblog
5.启动本地服务，连接localhost:4000查看网页形态
          jekyll serve --trace
          注：遇到报错：/Users/moyu/.gem/ruby/3.1.2/gems/jekyll-4.2.2/lib/jekyll/commands/serve/servlet.rb:3:in `require': cannot load such file -- webrick (LoadError)
          原因：从 Ruby 3.0 开始 webrick 已经不在绑定到 Ruby 中了，请参考链接： Ruby 3.0.0 Released 中的说明。webrick 需要手动进行添加。
          执行命令：bundle add webrick

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/moyu5021/slurm/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
