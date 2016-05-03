---
title: start
date: 2016-04-10 21:22:27
tags:
---

### notes for creating blog
install hexo command first
```sh
npm install -g hexo-cli
```

create a new folder for blog files (`npm install` will run automatically)
```sh
hexo init <folder>
```

create new article
(you can create the markdown file by yourself, but you will need to add some content on the top of the file)
(if the layout is not given, the `default_layout` from `_config.yml` will be used)
if there's space in the title, "-" will be used on filenames.
```sh
hexo new [layout] <title>
```

generate html files from markdown files
```sh
hexo generate
```

deploy to github (you may need to change `url`, `root` and `deploy` in `_config.yml` before deploy), for example:
```
url: http://wanderoo.github.io/myblog/
root: /myblog
deploy:
  type: git
  repo: https://github.com/wanderoo/myblog.git
  branch: gh-pages
```
and you need to install `hexo-deployer-git`
```sh
npm install hexo-deployer-git --save
```
then you can deploy
```sh
hexo deploy
```

start a local server for testing
```sh
hexo server
hexo server --port 8000 #override the default port(4000) to 8000, same as `-p`
hexo server --static    #only serve static files, same as `-s`
hexo server --log       #enable logger. override logger format
hexo server --debug     #enable debug print
```

#### beyond basic
watch files and generate when file changes
```sh
hexo generate --watch
#or
hexo generate -w
```

deploy after generation finishes
```sh
hexo generate --deploy
#or
hexo generate -d
```

### tips
there is **no** difference between
```sh
hexo generate --deploy
hexo deploy --generate
```

`_config.yml` is ignored when deploying to github, so run `hexo clean` after changing your theme. Then you can do `hexo deploy`.


### notes for markdown
**bold** *italic* (the space is necessary)
**bold***italic*(this is what happend when space missing)

no way for both **bold** *italic*

### Table test
speial variable for bash
```sh
$$ $! $? $- $* $@ $# $0 $1..$n
```
|Var|Description|
|-|-|
|`$$`|PID of the current script|
|`$!`|PID of the last background process|
|`$?`|exit code of last process|
|`$-`|all flags of `set`|
|`$*`|arguments list as "$1 $2 $3... $n"|
|`$@`|arguments list as "$1" "$2" "$3"... "$n"|
|`$#`|number of arguments|
|`$0`|script name|
|`$n`|the nth argument|


[search on baidu](https://www.baidu.com)
some images are available

![](https://img1.doubanio.com/view/movie_poster_cover/spst/public/p707509468.jpg)

some are not
![](https://img3.doubanio.com/view/photo/photo/public/p874840311.jpg)
