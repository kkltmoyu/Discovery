# 可视化组件or库
<b>本次调研终极目标：最好支持draggable、resizeable的轻量级，可自行定制图表及页面布局的，纯前端开源可视化图表展示系统（组件级、框架级也可），图表类型可切换。</b>  
语言：js  
兼容性要求：现代浏览器，不必考虑IE  
时间：2019.11.19
调研的主要内容如下，包含系统、组件库（框架）、体系三部分。
## 系统
以下系统均为纯前端，系统提供demo，demo内的数据均为mock
### [x-chart](https://github.com/yugasun/x-chart/tree/master)
小型系统，无法单独暴露其中组件，只能将整个项目作为脚手架，基于其上构建自己的功能。  
目前包含柱状图，折线图，饼图（无法相互切换）

### [vue-manager](https://github.com/luosijie/vue-manager)
技术栈：Vue2.0 + iView + ECharts，概况同上，图表包含饼图，柱状图，折线图，雷达图

### [Vue-Admin](https://github.com/lanux/Vue-Admin)
管理系统，脚手架项目

## 组件库（框架）
### [Viser](https://viserjs.github.io/)
基于阿里G2图标库封装，针对Vue，React，Angular三大框架有各自使用的单独版本，支持13种常见图表，实现较复杂代码量大，文档超级烂(写的不清楚)

### [BizCharts](https://bizcharts.net/products/bizCharts)
是基于阿里G2封装的React图表库，14+种图表，包含[场景模板](https://bizcharts.net/products/bizCharts/scaffolds),场景模板图表基于BizChart库

### [TOAST UI](https://ui.toast.com/tui-chart/)
### [CHARTIST](http://gionkunz.github.io/chartist-js/)
这两个库的两点也就是样式风格，对于图表的生成和配置相比于echarts的纯json方式要更加复杂

### [v-charts](https://v-charts.js.org/#/)
饿了么团队开发。在使用 echarts 生成图表时，经常需要做繁琐的数据类型转化、修改复杂的配置项，v-charts 的出现正是为了解决这个痛点。基于 Vue2.0 和 echarts 封装的 v-charts 图表组件，只需要统一提供一种对前后端都友好的数据格式设置简单的配置项，便可轻松生成常见的图表。支持图表类型同echarts。

## 体系
### [飞冰](https://github.com/alibaba/ice)
阿里前端体系一环，简单而友好的前端研发体系,基于物料的一站式可视化源码研发工作台。star：10000+  
1. 项目管理：覆盖项目研发的全流程管理，提供页面管理、路由管理、依赖管理、OSS 发布管理等能力；  
2. 工程管理：提供可视化工程配置和任务运行能力，屏蔽复杂的工程体系，降低开发门槛；  
3. 物料市场：提供丰富的垂直领域模板和区块(大组件)，可视化拖拽搭建页面，提升项目的开发效率；  
4. 定制工作台：通过 adapter 机制自由扩展工作台，打造开发者专属的一站式研发工作台，让开发者可以快速地创建和管理前端项目。  

优点：  
1. 各种物料可自行定制化（自己coding） 
2. 将复杂的工程化和项目管理等封装为可视化的ui界面

缺点：  
1. 各种物料主要为React技术栈准备，Vue技术栈资源相对少，对于Vue技术栈，目前的物料组件库使用Element-ui（饿了么官方开源），区块29个（包含条形图、漏斗图、环图、仪表盘图、饼图、雷达图、瀑布图），模板3个。  
2. 区块资源中的图是基于BizCharts进行开发,而不是echarts。  
3. 将复杂的工程化和项目管理等封装为可视化的ui界面，凡是封装必有性能损耗，以及奇葩bug。


<!--   不靠谱
### [zeu](https://github.com/shzlw/zeu)
### [markvis](https://github.com/geekplux/markvis)
-->

<!--
## 附加
### 可能有用库
1. [vue-draggable-resizable](https://github.com/mauricius/vue-draggable-resizable)
2. [图形化编辑、业务监控的大屏可视化方案dataV与Sugar比较](https://blog.csdn.net/hwhsong/article/details/83097924)
3. -->

## 总结
上述所有方案均无法完全满足本次调研的终极目标,最快捷的方式也只能在某个系统的基础上进行改动,具体需求具体分析。  
未找到完全符合本次调研终极目标的原因分析：  
1. 系统边界模糊。本次调研的目标严格上来讲，是需要一个具有能够自行配置页面结构的图表类纯前端可视化系统，通过对图表所需要的数据格式的约定，就可以实现无需对前端源代码进行大改动的前提下，通过后端接口传入不同的数据，以及前端不同的配置，实现想要的数据可视化。该系统的定位位于框架和系统之间，既包含框架的封装性和通用性，又要在其上加入一定的业务逻辑的封装（应对不同类型的图表不同需求的展示）。如果开发此类系统，很难划分该系统的边界，且无法抽象出完全通用的业务需求。这种系统多为定制化系统，无法开源，或者开源由于耦合过多业务而无人问津。  
2. 无法摆脱后端依赖。为了降低对现存后端系统的侵入，本系统期望为纯前端系统，但是如果没有后端的支撑，很难开发一个介于框架和成熟系统之间的可视化系统。

