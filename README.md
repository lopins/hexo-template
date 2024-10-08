<div align="right">
   <a href="README_CN.md">中文</a> | <strong>English</strong>
</div>

<img src="https://raw.githubusercontent.com/hexojs/logo/master/hexo-logo-avatar.png" alt="Hexo logo" width="100" height="100" align="right" />

<div align="center">

<h1> Hexo Template </h1>

<p>A fast, simple & powerful blog framework, powered by <a href="https://nodejs.org">Node.js</a>. Here is the template of it. </p>

</div>

<hr/>

<div align="center">
<a href="https://lopins.github.io/hexo-template">Demo</a> | 
<a href="https://hexo.io">Official</a> | 
<a href="https://hexo.io/docs/">Docs</a> | 
<a href="https://hexo.io/zh-cn/api/">API</a> | 
<a href="https://hexo.io/plugins/">Plugins</a> | 
<a href="https://hexo.io/themes/">Themes</a>
</div>

<hr/>

## Get Started

### Set your site url at **line 16**

For example, if you use GitHub Page, set url as `https://username.github.io/projectname`:

```yml
url: https://lopins.github.io/hexo-template
```

### Set your project name at **line 107**

if your project name is `username` or `username.github.io`, just remove it at the end of `_config.yml`: 

```yml
root: /hexo-template
```

### Configure and Enable theme

1. pull theme into `themes/` and update it.

`git submodule add git@github.com:litten/hexo-theme-yilia.git themes/yilia && git submodule update --init --recursive`

2. update `theme: yilia` and configure other fields in `_config.yml`

3. configure the theme in `_config.yilia.yml` or into  `themes/yilia` to configure the theme in `_config.yml`

### Push to Github

`git add . && git commit -m ':wrench:docs(themes): Add or update configuration files' && git push origin main`

### Publish Article

1. Install

Click "Use this template" -> "Create a new repository"

![Use this template to create a new repository](https://github.com/user-attachments/assets/5e9a2358-4402-4dc8-be82-441dac86f4e3)

2. Set up

Set up and enable GitHub Pages service

![Set up and enable GitHub Pages service](https://github.com/user-attachments/assets/001b6c80-f4d7-40a9-92fe-ef1c5112dccb)

3. Publish

Publish an article on the "hexo branch" of Github.

![Publish an article on the "hexo branch" of Github.](https://github.com/user-attachments/assets/416a223a-837b-42d0-910e-0cb55e3ea284)

## Notice

### **Submodule** to Change Theme

```
# Add Submodule - Upadte Submodule
git submodule add git@github.com:litten/hexo-theme-yilia.git themes/yilia
git submodule update --init --recursive

# Delete Submodule
git submodule deinit -f themes/yilia
rm -rf .git/modules/themes/yilia
rm -rf themes/yilia

# Display Submodule - Pull Submodule - Sync Submodule
git submodule status
git submodule foreach git pull origin main
git submodule sync
```

### Permission

If you meet the problem like `remote: Permission to xxx denied to github-actions[bot].` 

When you push your changes, you need to give the permission to the `github-actions[bot]` in your repo's.

By following the steps below: `Settings -> Actions -> General -> Workflow permissions -> Read and write permissions -> Save`.

## License

[MIT License](LICENSE).
