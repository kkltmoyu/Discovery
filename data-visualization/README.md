# 可视化组件or库
<b>本次调研目标：最好支持draggable，resizeable的轻量级可视化图表展示库，组件级或框架级。</b>  
语言：js  
兼容性要求：现代浏览器，不必考虑IE  
时间：2019.11.19

## 系统
### [x-chart](https://github.com/yugasun/x-chart/tree/master)
小型系统，无法单独暴露其中组件，只能将整个项目作为脚手架，基于其上构建自己的功能。  
目前包含柱状图，折线图，饼图（无法相互切换）

### [vue-manager](https://github.com/luosijie/vue-manager)
技术栈：Vue2.0 + iView + ECharts，概况同上，图表包含饼图，柱状图，折线图，雷达图

## 组件库（框架）
### [Viser](https://viserjs.github.io/)
基于阿里G2图标库封装，针对Vue，React，Angular三大框架有各自使用的单独版本，支持13种常见图表，实现较复杂代码量大，文档超级烂(写的不清楚)

### [BizCharts](https://bizcharts.net/products/bizCharts)
是基于阿里G2封装的React图表库，14+种图表，包含[场景模板](https://bizcharts.net/products/bizCharts/scaffolds),场景模板图标基于BizChart库

### [TOAST UI](https://ui.toast.com/tui-chart/)
### [CHARTIST](http://gionkunz.github.io/chartist-js/)

### [v-charts](https://v-charts.js.org/#/)
饿了么团队开发。在使用 echarts 生成图表时，经常需要做繁琐的数据类型转化、修改复杂的配置项，v-charts 的出现正是为了解决这个痛点。基于 Vue2.0 和 echarts 封装的 v-charts 图表组件，只需要统一提供一种对前后端都友好的数据格式设置简单的配置项，便可轻松生成常见的图表。支持图表类型同echarts。


## 解决方案
### [飞冰](https://github.com/alibaba/ice)
阿里前端体系一环，简单而友好的前端研发体系,基于物料的一站式可视化源码研发工作台。  
1. 项目管理：覆盖项目研发的全流程管理，提供页面管理、路由管理、依赖管理、OSS 发布管理等能力；  
2. 工程管理：提供可视化工程配置和任务运行能力，屏蔽复杂的工程体系，降低开发门槛；  
3. 物料市场：提供丰富的垂直领域模板和区块(组件)，可视化拖拽搭建页面，提升项目的开发效率；  
4. 定制工作台：通过 adapter 机制自由扩展工作台，打造开发者专属的一站式研发工作台，让开发者可以快速地创建和管理前端项目。  


<!--   不靠谱
## [zeu](https://github.com/shzlw/zeu)

-->

## 方案9.markvis
https://github.com/geekplux/markvis

## 方案10.Vue-Admin
https://github.com/lanux/Vue-Admin

## 附加
### 可能有用库
1. [vue-draggable-resizable](https://github.com/mauricius/vue-draggable-resizable)
2. [图形化编辑、业务监控的大屏可视化方案dataV与Sugar比较](https://blog.csdn.net/hwhsong/article/details/83097924)

