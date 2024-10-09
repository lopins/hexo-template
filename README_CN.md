<div align="right">
   <strong>中文</strong> | <a href="README.md">English</a>
</div>

<img src="https://raw.githubusercontent.com/hexojs/logo/master/hexo-logo-avatar.png" alt="Hexo logo" width="100" height="100" align="right" />

<div align="center">

<h1> Hexo Template </h1>

<p>一个快速、简洁且高效基于 <a href="https://nodejs.org">Node.js</a>的博客框架。 这是它的模板。 </p>

</div>

<hr/>

<div align="center">
<a href="https://lopins.github.io/hexo-template">演示</a> | 
<a href="https://hexo.io">官网</a> | 
<a href="https://hexo.io/docs/">文档</a> | 
<a href="https://hexo.io/zh-cn/api/">接口</a> | 
<a href="https://hexo.io/plugins/">插件</a> | 
<a href="https://hexo.io/themes/">主题</a>
</div>

<hr/>

## 快速开始

### 在 `_config.yml` 的16行设置你的站点地址

例如，如果你使用Github Pages默认地址，可以设置为： `https://username.github.io/projectname`:

```yml
url: https://lopins.github.io/hexo-template
```

### 在 `_config.yml` 的107行设置你的项目ID

如果你的项目ID为 `username` or `username.github.io`, 你只需要在 `_config.yml`的最后一行设置: 

```yml
root: /hexo-template
```

### [配置主题](https://github.com/lopins/hexo-template/issues/2)

1. 拉取主题并进入 `themes/` 并更新相关信息(以下二选一)

   `git submodule add git@github.com:litten/hexo-theme-yilia.git themes/yilia && git submodule update --init --recursive`

   `git clone git@github.com:litten/hexo-theme-yilia.git themes/yilia && rm -rf themes/yilia/.git`

2. 在 `_config.yml` 中更新 `theme: yilia` 并且配置其他信息 

3. 在 `_config.yilia.yml` 或者进入  `themes/yilia` 中 `_config.yml` 文件配置主题相关

4. (**可选**)如果主题有依赖插件，还需要执行 `npm install && npm install hexo-xxx hexo-yyy hexo-zzz --save`

5. 执行 `git add . && git commit -m ':wrench:docs(themes): Add or update configuration files' && git push origin main` 提交更改

### [发布文章](https://github.com/lopins/hexo-template/issues/1)

1. 启用站点

   点击 "Use this template" -> "Create a new repository"

![1. Create a new repository](https://github.com/user-attachments/assets/0e3053a1-4270-489f-80fd-2059d1f4dbbf)

2. 配置站点

   设置并且启用 GitHub Pages 服务

![2. Set up GitHub Pages branch](https://github.com/user-attachments/assets/ea36bec9-4a11-4e76-8e82-97230deab530)

3. 发布文章

   发布文章在 `hexo` 分支。

![3. Write or Upload an Markdown file](https://github.com/user-attachments/assets/4edbdeb8-fd3f-4173-9013-15134772883d)

## 特别注意

### 使用 **Submodule** 切换主题

```
# Add Submodule - Upadte Submodule
git submodule add git@github.com:litten/hexo-theme-yilia.git themes/yilia
git submodule update --init --recursive

# Delete Submodule
git submodule deinit -f themes/yilia
rm -rf .git/modules/themes/yilia
rm -rf themes/yilia
git config --remove-section submodule.themes/yilia
git config -f .gitmodules --remove-section submodule.themes/yilia
git rm --cached themes/yilia
git add . && git commit -m 'Update .gitmodules before removing submodule'

# Display Submodule - Pull Submodule - Sync Submodule
git submodule status
git submodule foreach git pull origin main
git submodule sync
```

### 权限问题

如果你遇到类似 `remote: Permission to xxx denied to github-actions[bot].` 

当你推送更改时，你需要设置仓库的 `github-actions[bot]` 权限.

设置步骤: `Settings -> Actions -> General -> Workflow permissions -> Read and write permissions -> Save`.

## 开源协议

[MIT License](LICENSE).
