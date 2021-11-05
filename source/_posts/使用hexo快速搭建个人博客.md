---
title: 使用hexo快速搭建个人博客
date: 2021-09-22 18:59:29
categories: 
- 记录
tags: 
- hexo
- github
---

## 新建仓库

假设你已经有github账号，并且会基本操作。新建名称<usernmae>.github.io的仓库，设置为公共，不要私有。
<!--more-->

## 安装hexo

1. 全局安装

   ```
   npm install -g hexo-cli
   ```

2. 局部安装

   ```
   npm install hexo
   ```
## 建站

新建一个文件夹，在终端中打开，执行以下命令

```
hexo init	// 初始化
npm install // 安装依赖
hexo s		// 启动项目
```

## 部署

1. 安装 hexo-deployer-git

   ```
   npm install hexo-deployer-git --save
   ```

2. 在 **_config.yml**（如果有已存在的请删除）添加如下配置

   ```
   deploy:
     type: git
     repo: https://github.com/<username>/<username>.github.io
     # repo: https://github.com/kaipengHan/kaipengHan.github.io
     branch: gh-pages
   ```

3. 运行  hexo clean && hexo deploy

4. 查看 *username*.github.io 上的网页是否部署成功。

## 新建文章

Hexo 有三种默认布局：`post`、`page` 和 `draft`。默认为post，可以通过修改 `_config.yml` 中的 `default_layout` 参数来指定默认布局。

```
hexo new [layout] <title>
```

## 主题

这里介绍使用[NexT](https://github.com/theme-next/hexo-theme-next)，更多主题[请参考](https://hexo.io/themes/)，每个主题底部都有对应的文档地址，大家使用哪个可以参考。

### 安装

```
 git clone https://github.com/theme-next/hexo-theme-next themes/next
```

### 更新

```
cd themes/next
git pull
```

### 在 **_config.yml**修改如下配置

```
theme: next
```

### 关于NexT文档

[旧文档](http://theme-next.iissnan.com/)的下载主题不要在使用了，因为该项目已经迁移到了[新地址](https://github.com/theme-next/hexo-theme-next)，要克隆新地址的仓库。不过这个文档中的其他大部分设置还是可以参考进行设置的。[新地址](https://github.com/theme-next/hexo-theme-next)上没找到详细的文档。