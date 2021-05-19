## 介绍
@vue/cli包括了
vue/cli-service
vue/cli-plugin
## 安装
```sh
npm install -g @vue/cli
```
检查
```sh
vue --version
```
升级全局包
```sh
npm update -g @vue/cli
```
升级插件
```sh
vue upgrade
```
# 基础
## 快速原型开发
自动查找当前目录的app.vue或者main.js、index.js等入口文件
```sh
vue serve
```
将目标文件构建成一个生产环境的包并用来部署
```sh
vue build
```
## 创建一个项目
```sh
vue create [项目名]
```
然后进行一些设置
```sh
vue ui
```
可以图形化地管理界面
## 插件和preset
插件可以修改webpack的内部配置,还能外vue-cli-service注入命令
```sh
vue add [插件名]
```
也可以在GUI中增加插件

