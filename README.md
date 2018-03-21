# React NC Pages Application

> 基于webpack+react搭建基本快速开发脚手架并使用强大的集成开发工具[ uba ](https://github.com/iuap-design/tinper-uba)

### 说明

- 采用多页面react开发模式

- 本脚手架依赖于前端集成开发工具[ uba ](https://github.com/iuap-design/tinper-uba)，项目生成的时候需要安装全局工具命令来使用，参与开发人员无需重复安装全局使用。

- 集成市面上常规的使用插件等配置，可以满足常规开发需求，无需繁琐复杂的配置项，简单、干净、舒服。

- 依赖强大的集成开发工具 `uba` 内置 `数据模拟`、`代理请求`、`静态托管`、`开放配置`等功能.

- 方便开发人员在快速搭建`react`前端开发项目，无需学习复杂配置环境，拆箱即用.


## 参数

> uba server --port 4000 --noInfo --logLevel debug --chunks --noOpen

- `--noProcess` 不显示进度百分比
- `--logLevel` 日志级别，默认：info 其他为：trace,debug,info,warn,error,silent
- `--chunks` 不显示详细的chunks信息
- `--port` 服务器端口设置，默认：3000，如冲突随机端口
- `--noOpen` 不自动打开浏览器


### 安装与使用

1. 安装`uba` 命令：`npm install uba -g`.

2. 启动开发`npm run dev`,稍等片刻会自动打开默认浏览器显示.

3. 开发完毕后，使用命令`npm run build`来产出所需的静态资源依赖文件.

4. 享受集成开发工具`uba`给你带来的方便体验来开发吧！

### 默认内置

- `react 15.6.1`、`react-dom 15.6.1`、`webpack`.
- `babel`、`ES5\6`、`postcss`、`Less`、`图片处理`、`字体处理`、`热部署`.

### 资源说明

```base

├── LICENSE
├── README.md
├── mock                        # 数据模拟存放文件夹
│   └── api
│       └── user
│           ├── get.json
│           └── post.json
├── package.json
├── postcss.config.js           # postcss配置
├── src                         # 开发源代码
│   ├── assets                  # 资源存放
│   │   └── images
│   │       ├── favicon.png
│   │       └── jay.jpg
│   ├── components              # 组件
│   │   └── Test
│   │       ├── index.css
│   │       └── index.js
│   ├── pages                   # 多页面入口
│   │   ├── index               # 页面(index.html)
│   │   │   ├── index.css
│   │   │   ├── index.html
│   │   │   └── index.js
│   │   └── login
│   │       └── user            # 页面(login/user.html)
│   │           ├── index.css
│   │           ├── index.html
│   │           └── index.js
│   └── static                  # 静态资源
│       └── js
│           └── demo.js
├── uba.config.js               # uba集成工具核心配置文件
└── uba.mock.js                 # uba数据模拟配置

```

### 多页面配置

项目下`src/pages/*`里面放着我们的多页面文件，其中`pages/index`就是首页，会产出www.xxx.com/index.html的页面。

举例说明：我们要添加一个一级页面，在pages下面新建文件夹，如下：

```base
├── user
│   ├── index.css
│   ├── index.html
│   └── index.js
```
产出页面：`http://127.0.0.1:3000/user.html`

匹配规则是，当pages下有一个文件夹，并且里面包含index.html,index.js的话，那么就是一个有效的页面。除此之外，其他均不生效！！！
