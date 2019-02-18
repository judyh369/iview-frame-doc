## 简介

> custom-admin是套采用前后端分离开发模式，基于Vue的后台管理系统前端解决方案

整个框架基于iview组件库开发的，iview是一套基于 Vue.js 的高质量UI 组件库。官方([文档](https://www.iviewui.com/))。

custom-admin采用Webpack4.0 + Vue-cli3.0作为基本开发环境。内置了开发后台管理系统常用的逻辑功能，和开箱即用的业务组件，旨在让开发者能够以最小的成本开发后台管理系统，降低开发量。
## 目录结构
```bash
├── vue.config  webpack配置（Vue-cli3.0）
├── public  打包所需静态资源
└── src
    ├── api  AJAX请求
    └── assets  项目静态资源
        ├── icons  自定义图标资源
        └── images  图片资源
    ├── components  公共组件
    ├── config  项目运行配置
    ├── utils  封装工具函数
    ├── mock  mock模拟数据
    ├── router  路由配置
    ├── store  Vuex配置
    ├── styles  样式文件
    └── views  页面文件
```

## 资源
vue.config.js配置说明：https://cli.vuejs.org/zh/guide/webpack.html  
mockjs的文档：http://mockjs.com/  (可以直接看示例)


## 说明

风格指南章节对实际项目开发的一些约定做了说明


