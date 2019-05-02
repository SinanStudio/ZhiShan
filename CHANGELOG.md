# 更新日志

## 项目初始化

### 安装

```
composer config -g repo.packagist composer https://packagist.laravel-china.org
composer selfupdate
composer global update
composer create-project --prefer-dist laravel/laravel ZhiShan
```

### 修改版本忽略文件

**.gitignore**:

```
/node_modules
/public/hot
/public/storage
/storage/*.key
/vendor
.env
.phpunit.result.cache
Homestead.json
Homestead.yaml
npm-debug.log
yarn-error.log
.idea
```

### package.json 修改


### 版本管理

**设置当前项目的用户名/邮箱**

```
git init
git config --local user.name "JianNei"
git config --local user.email "longjian.huang@aliyun.com"
git config --global credential.helper store
```

**设置当前分支为默认推送分支**

```
git config --global push.default simple
```

**其他**

```
echo "# some" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:JianNei/Shan.git
git push -u origin master
```

## 工具

### deployer

composer 安装方式：

* 全局安装：`composer global require deployer/deployer -vvv`
* 项目安装：`composer require deployer/deployer --dev`

~~选择使用项目安装方式，目的是可以在 composer.json 文件中看到项目的依赖环境。~~

疑问：
* .env 文件部署时无法配置
* deploy.php 文件中的ip域名配置是否可以考虑配置到 .env 文件
* .env 文件是否可以读取本地 .env 配置然后生成文件到 shared 目录
* 图形化工具：配置生成 deploy.php

### travis-ci

### StyleCi

### phpstorm 插件

## 扩展包使用

### 前端

* commitizen/cz-cli：规范 git message 提交


```
npm install -D commitizen cz-conventional-changelog
# OR yarn add -D commitizen cz-conventional-changelog

npm run commit
# OR yarn commit
```

* vuepress：项目文档

```
yarn add -D vuepress@next
yarn add -D @vuepress/plugin-back-to-top@next
yarn add -D @vuepress/plugin-medium-zoom@next
```

* element-ui:

```
yarn add -D vue
yarn add -D element-ui
#OR npm i element-ui -S
```

### 后端

* laravel-wechat：https://github.com/overtrue/laravel-wechat
* barryvdh/laravel-debugbar：https://github.com/barryvdh/laravel-debugbar
* barryvdh/laravel-ide-helper：https://github.com/barryvdh/laravel-ide-helper
* mpociot/laravel-test-factory-helper

```
// 执行 composer update

"post-update-cmd": [
    "Illuminate\\Foundation\\ComposerScripts::postUpdate",
    "php artisan ide-helper:generate",
    "php artisan ide-helper:meta"
]
```

## TODO
