---
title: 标签 
layout: page 
type: tags 
tag: Jekyll
---

# jekyll发布文章不显示

昨天尝试更改博客布局，修改顶部栏目，添加文件后发现没有效果

今天发现新增博客也没有刷新

## 原因

jekyll编译错误

到博客绑定的邮箱查看报错日志



![image-20211223170603288](https://github.com/modiman/modiman.github.io/blob/gh-pages/docs/_posts/imgs/image-20211115125643082.png?raw=true)



![image-20211223170603288](https://github.com/modiman/modiman.github.io/blob/gh-pages/docs/_posts/imgs/image-20211115125724429.png?raw=true)

发现是这个yml文件格式有错误，这是昨天为了新增栏目添加的文件。俺也不知道怎么改，一想留着也没用，最近也没精力修改博客主题，干脆删了。

以后有时间再重新自定义主题，现在只使用基本功能。



## 修改主题

**改为NExT**

1. 安装Ruby并添加环境变量

2. 更换gem镜像源为中国，不然无法继续

   1. ```bash
      $ gem sources --add https://gems.ruby-china.com/ --remove https://rubygems.org/
      $ gem sources -l
      https://gems.ruby-china.com
      # 确保只有 gems.ruby-china.com
      ```

3. 安装指定版本`bundler`

   1. ```bash
      gem install bundler -v 1.17.1
      ```

4. 下载 NexT 主题：

   1. ```bash
      $ git clone https://github.com/Simpleyyt/jekyll-theme-next.git
      $ cd jekyll-theme-next
      ```

5. 安装依赖： 

   1. ```bash
      $ bundle install
      ```

6. 安装jekyll

   1. ```bash
      gem install jekyll
      ```

   2. 安装过程中可能会报错，根据提示下载缺失的组件

7. 运行 Jekyll：

   1. ```bash
      $ bundle exec jekyll server
      ```

