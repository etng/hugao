---
title: "Start Hugao"
title: "开始胡搞"
summary: "不管是不是胡搞，只要开搞了就会有成果;一直是草稿，胡搞到底！"
date: 2023-04-07T11:31:49+08:00
lastmod: 2023-04-07T11:31:49+08:00
categories:
tags:
comments: true
showtoc: true
searchHidden: false
hidemeta: false
draft: false
weight:
cover:
    image: "cover.webp"
    alt: "cover"
    relative: true
    hidden: true
---
一个人如果太懒散了实在不好
![](lazy.png)

```

hugo new site hugao -f yml
cd hugao
git init

git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod


cat<<EOT>config.yml
# 起始 URL（换成您自己的域名）
baseURL: 'https://hugao.pages.dev'
# 网站标题
title: '胡搞'
# 每页显示的文章数量
paginate: 5
# 主题名称
theme: PaperMod
# 语言代码（zh-简体中文）
languageCode: 'zh'
DefaultContentLanguage: 'zh'
# 是否有 CJK 语言（中-日-韩）
hasCJKLanguage: true

# 是否生成 robots.txt
enableRobotsTXT: true

# 是否构建草稿
buildDrafts: false
# 是否构建未来的文章
buildFuture: false
# 是否构建过期的文章
buildExpired: false
# 是否启用 Emoji
enableEmoji: true
# 是否启用 Git 信息
enableGitInfo: false

# Google Analytics ID
googleAnalytics: ''

# 压缩输出静态文件
minify:
  # 是否不压缩 XML 文件
  disableXML: true
  minifyOutput: true

# 全局配置
params:
  env: production
  # 网站标题
  title: '胡搞'
  # 网站描述
  description: '胡搞 用了PaperMod我骄傲了吗？'
  # 网站关键词（大部分搜索引擎已放弃，可注释掉）
  # keywords: [Blog, Portfolio, PaperMod]

  # 网站作者
  author: '胡高'
  # 多个作者写法
  # author: ["Me", "You"]

  # OpenGraph / Twitter Card 预览图片（/static 下面的文件名称）
  images: ['opengraph.webp']
  # 日期格式
  DateFormat: '2006-01-02'
  # 默认主题
  defaultTheme: auto # dark, light
  # 是否启用主题切换按钮
  disableThemeToggle: false
  # 是否启用阅读时间展示
  ShowReadingTime: true
  # 是都启用分享按钮
  ShowShareButtons: true
  ShowPostNavLinks: true
  # 是否启用面包屑导航
  ShowBreadCrumbs: true
  # 是否显示代码复制按钮
  ShowCodeCopyButtons: false
  # 是否显示字数统计
  ShowWordCount: true
  # 是否在页面显示 RSS 按钮
  ShowRssButtonInSectionTermList: true
  UseHugoToc: true
  disableSpecial1stPost: false
  # 是否禁用首页滚动到顶部
  disableScrollToTop: false
  # 是否启用评论系统
  comments: false
  # 是否隐藏 Meta 信息
  hidemeta: false
  # 是否隐藏文章摘要
  hideSummary: false
  # 是否显示目录
  showtoc: false
  # 是否默认展开文章目录
  tocopen: false

  assets:
    # disableHLJS: true # to disable highlight.js
    # disableFingerprinting: true

    # 网站 Favicon 图标相关信息
    # 可在 https://realfavicongenerator.net/ 生成
    # 将图片复制到 /static 目录下
    # 然后修改下面代码中的文件名
    favicon: '<link / abs url>'
    favicon16x16: '<link / abs url>'
    favicon32x32: '<link / abs url>'
    apple_touch_icon: '<link / abs url>'
    safari_pinned_tab: '<link / abs url>'

  label:
    # 使用文本替代 Logo 标签
    text: '胡搞'
    # 网站 Logo 图片（/static 下面的文件名称）
    icon: /apple-touch-icon.png
    # 图标高度
    iconHeight: 35

  # 主页展示模式
  # 个人信息模式
  profileMode:
    enabled: false # needs to be explicitly set
    title: ExampleSite
    subtitle: 'This is subtitle'
    imageUrl: '<img location>'
    imageWidth: 120
    imageHeight: 120
    imageTitle: my image
    buttons:
      - name: Posts
        url: posts
      - name: Tags
        url: tags

  # 主页 - 信息模式（默认）
  homeInfoParams:
    Title: "Hi there \U0001F44B"
    Content: Welcome to 胡搞, this is a example of Hugo and PaperMod

  #  主页 - 信息模式 图标展示
  socialIcons:
    # - name: twitter
    #   url: "https://twitter.com/"
    # - name: stackoverflow
    #   url: "https://stackoverflow.com"
    - name: github
      url: 'https://github.com/etng/hugao'

  # 站长验证
  analytics:
    google:
      SiteVerificationTag: ''
    bing:
      SiteVerificationTag: ''
    yandex:
      SiteVerificationTag: ''

  # 文章封面设置
  cover:
    hidden: true # hide everywhere but not in structured data
    hiddenInList: true # hide on list pages and home
    hiddenInSingle: true # hide on single page

  # 关联编辑
  editPost:
    URL: 'https://github.com/etng/hugao/edit/master/content/posts'
    Text: 'Edit on GitHub' # edit text
    appendFilePath: true # to append file path to Edit link

  # for search
  # https://fusejs.io/api/options.html
  fuseOpts:
    isCaseSensitive: false
    shouldSort: true
    location: 0
    distance: 1000
    threshold: 0.4
    minMatchCharLength: 0
    keys: ['title', 'permalink', 'summary', 'content']

# 顶部导航栏
menu:
  main:
    - identifier: '首页'
      name: '首页'
      url: /
      weight: 1
    - identifier: '分类'
      name: '分类'
      url: /categories/
      weight: 10
    - identifier: '标签'
      name: '标签'
      url: /tags/
      weight: 20
    - identifier: '仓库'
      name: '仓库'
      url: https://github.com/etng/hugao
      weight: 30
# Read: https://github.com/adityatelange/hugo-PaperMod/wiki/FAQs#using-hugos-syntax-highlighter-chroma
pygmentsUseClasses: true
markup:
  highlight:
    noClasses: false
    # anchorLineNos: true
    # codeFences: true
    # guessSyntax: true
    # lineNos: true
    # style: monokai

privacy:
  vimeo:
    disabled: true
    enableDNT: true
    simple: true

  twitter:
    disabled: true
    enableDNT: true # 是否启用添加“请勿跟踪” HTTP 头。
    simple: true # 如果启用简单模式，将建立一个静态的、无 JS 版本的推文。

  instagram:
    disabled: true
    simple: true

  youtube:
    disabled: true
    privacyEnhanced: true

services:
  instagram:
    disableInlineCSS: true # 禁用 Hugo 提供的内联样式
  twitter:
    disableInlineCSS: true # 禁用 Hugo 提供的内联样式

EOT
cat<<'EOT'>archetypes/posts.md
---
title: "{{ replace .Name "-" " " | title }}"
summary: ""
date: {{ .Date }}
lastmod: {{ .Date }}
categories:
tags:
comments: true
showtoc: true
searchHidden: false
hidemeta: false
draft: true
weight:
cover:
    image: "cover.webp"
    alt: "cover"
    relative: true
    hidden: true
---
EOT

# 建议使用 Hugo 的 [Page Bundle](https://gohugo.io/content-management/page-bundles/) 模式来管理静态资源，此时我们的第一篇示例文章目录结构如下
hugo new posts/start-hugao/index.md
hugo new archives/_index.md


cat<<'EOT'>.gitignore
.DS_Store
# Generated files by hugo
/public/
/resources/_gen/
/assets/jsconfig.json
hugo_stats.json

# Executable may be added to repository
hugo.exe
hugo.darwin
hugo.linux

# Temporary lock file while building
/.hugo_build.lock
EOT

```

```
cat<<'EOT'>readme.md
# 胡搞博客，欢迎投稿
# 偶有收获，定属意外
EOT
```

```
hugo sever

# 带上 -D 参数可以预览草稿
hugo server -D
```


```
open https://github.com/new
git remote add origin git@github.com:etng/hugao.git
```

https://pages.dev/

framework hugo
HUGO_VERSION	0.111.3

Add the following CNAME record:

Name
make
Click to copy
Target
hugao.pages.dev
Click to copy


```
# 克隆 Git 子模块
cd Blog && git submodule update --init --recursive
# 启动 Hugo 预览服务器
hugo server -D
# 更新主题
git submodule update --remote --merge
```

```
mkdir -p layouts/partials
cp themes/PaperMod/layouts/partials/footer.html layouts/partials 
```