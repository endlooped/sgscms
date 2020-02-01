# sgscms

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


# sgscms
## SGS检测办公流程自动化管理系统

`假设项目目录是 sgscms`

`该项目前端是基于vuejs搭建的 需要先安装 nodejs`

`然后通过 npm 安装vue`

```shell
endloopdeMBP:sgscms endloop$ cd sgscms
endloopdeMBP:sgscms endloop$ node -v
v12.1.0
endloopdeMBP:sgscms endloop$ npm install vue
endloopdeMBP:sgscms endloop$ vue -V
2.9.6
endloopdeMBP:sgscms endloop$ 
```

在用 Vue 构建大型应用时推荐使用 NPM 安装[1]。
NPM 能很好地和诸如[webpack](https://webpack.js.org/)或 [Browserify](http://browserify.org/) 模块打包器配合使用。同时 Vue 也提供配套工具来开发单文件组件。

### 命令行工具 (CLI)
Vue 提供了一个官方的 [CLI](https://github.com/vuejs/vue-cli)，为单页面应用 (SPA) 快速搭建繁杂的脚手架。它为现代前端工作流提供了 batteries-included 的构建设置。只需要几分钟的时间就可以运行起来并带有热重载、保存时 lint 校验，以及生产环境可用的构建版本。更多详情可查阅 [Vue CLI](https://cli.vuejs.org/) 的文档。

### 关于旧版本
>Vue CLI 的包名称由 vue-cli 改成了 @vue/cli。 如果你已经全局安装了旧版本的 vue-cli (1.x 或 2.x)，你需要先通过 npm >uninstall vue-cli -g 或 yarn global remove vue-cli 卸载它。

```shell
endloopdeMBP:sgscms endloop$ npm install -g @vue/cli
```
`或者需要sudo`
```shell
endloopdeMBP:sgscms endloop$ npm install -g @vue/cli
```
`或者需要sudo 并带 --unsafe-perm`
```shell
endloopdeMBP:sgscms endloop$ npm install -g --unsafe-perm @vue/cli
```
`安装好后`
```
endloopdeMBP:sgscms endloop$ vue --version
@vue/cli 4.1.2
endloopdeMBP:sgscms endloop$ 
```

`可以使用 vue serve 和 vue build 命令对单个 *.vue 文件进行快速原型开发，不过这需要先额外安装一个全局的扩展`
```
npm install -g @vue/cli-service-global
```

`这里使用 vue create 来创建项目`
```
endloopdeMBP:sgscms endloop$ vue create sgscms
/usr/local/lib/node_modules/@vue/cli/node_modules/vue-template-compiler/index.js:10
  throw new Error(
  ^

Error: 

Vue packages version mismatch:

- vue@2.6.10 (/usr/local/lib/node_modules/vue/dist/vue.runtime.common.js)
- vue-template-compiler@2.6.11 (/usr/local/lib/node_modules/@vue/cli/node_modules/vue-template-compiler/package.json)

This may cause things to work incorrectly. Make sure to use the same version for both.
If you are using vue-loader@>=10.0, simply update vue-template-compiler.
If you are using vue-loader@<10.0 or vueify, re-installing vue-loader/vueify should bump vue-template-compiler to the latest.

    at Object.<anonymous> (/usr/local/lib/node_modules/@vue/cli/node_modules/vue-template-compiler/index.js:10:9)
    at Module._compile (internal/modules/cjs/loader.js:759:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:770:10)
    at Module.load (internal/modules/cjs/loader.js:628:32)
    at Function.Module._load (internal/modules/cjs/loader.js:555:12)
    at Module.require (internal/modules/cjs/loader.js:666:19)
    at require (internal/modules/cjs/helpers.js:16:16)
    at Object.<anonymous> (/usr/local/lib/node_modules/@vue/cli/node_modules/vue-jscodeshift-adapter/src/parse-sfc.js:1:18)
    at Module._compile (internal/modules/cjs/loader.js:759:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:770:10)
endloopdeMBP:sgscms endloop$ 
```
`vue@2.6.10 与 vue-template-compiler@2.6.11 版本不匹配，将 vue@2.6.10 升级到 vue@2.6.11 即可`
```
endloopdeMBP:sgscms endloop$ sudo npm install -g vue@2.6.11
+ vue@2.6.11
updated 1 package in 1.061s
endloopdeMBP:sgscms endloop$ cd ..
endloopdeMBP:Public endloop$ vue create sgscms
...
🎉  Successfully created project sgscms.
👉  Get started with the following commands:

 $ cd sgscms
 $ npm run serve

endloopdeMBP:Public endloop$ cd sgscms/
endloopdeMBP:sgscms endloop$ ll 
total 872
-rw-r--r--    1 endloop  staff     318  2  1 14:24 README.md
-rw-r--r--    1 endloop  staff      73  2  1 14:23 babel.config.js
drwxr-xr-x  820 endloop  staff   26240  2  1 14:24 node_modules
-rw-r--r--    1 endloop  staff  432862  2  1 14:24 package-lock.json
-rw-r--r--    1 endloop  staff     836  2  1 14:23 package.json
drwxr-xr-x    4 endloop  staff     128  2  1 14:23 public
drwxr-xr-x    6 endloop  staff     192  2  1 14:23 src
endloopdeMBP:sgscms endloop$
···