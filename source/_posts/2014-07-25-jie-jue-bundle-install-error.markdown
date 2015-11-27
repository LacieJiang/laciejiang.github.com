---
published: false
layout: post
title: "解决Bundle install error"
date: 2014-07-25 22:30:06 +0800
comments: true


Bundle install error
===============
我的mac系统是10.9.3, 系统安装有xcode5,xcode6 beta,在配置octopress的时候，总是出现以下错误：
```
Gem::Installer::ExtensionBuildError: ERROR: Failed to build gem native extension.    /System/Library/Frameworks/Ruby.framework/Versions/2.0/usr/bin/ruby extconf.rbmkmf.rb can't find header files for ruby at /System/Library/Frameworks/Ruby.framework/Versions/2.0/usr/lib/ruby/include/ruby.hGem files will remain installed in /var/folders/nr/fjksglz55z906kj454dp27dc0000gn/T/bundler20140725-74454-o8bwh5/RedCloth-4.2.9/gems/RedCloth-4.2.9 for inspection.Results logged to /var/folders/nr/fjksglz55z906kj454dp27dc0000gn/T/bundler20140725-74454-o8bwh5/RedCloth-4.2.9/gems/RedCloth-4.2.9/ext/redcloth_scan/gem_make.outAn error occurred while installing RedCloth (4.2.9), and Bundler cannotcontinue.Make sure that `gem install RedCloth -v '4.2.9'` succeeds before bundling.```
解决办法：
执行以下操作：
切换Xcode用到的SDK和命令行工具的目录:
```
sudo xcode-select --switch /Applications/Xcode.app
```
参考：
<http://handy-wang.iteye.com/blog/2022821>