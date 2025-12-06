> 该方法适用于**1.10**及之后的**版本**

## 进入 Typora 官方中文站


下载并安装，假设你的安装路径为 D:/App/Typora

关闭所有Typora相关进程

## 用VSCode打开 D:/App/Typora

全局搜索，将

```bash
e.hasActivated="true"==e.hasActivated
```

改为

```bash
e.hasActivated="true"=="true"
```

打开 Typora，已激活

![](https://xz131714.github.io/PicBed/20251206172136407.png)
## 自动关闭弹窗
Typora\resources\page-dist\static\js\0.99879679.chunk.js
```bash
//粘贴至开头
setTimeout(function() { document.querySelector('.default-btn.secondary-btn').click(); }, 150); 
```
隐藏未激活标签
Typora\resources\window.html
```html
<!-- <!doctype html><html lang="en"><head>后添加 -->
<style>body>div[role="button"]{visibility:hidden;}</style>
```