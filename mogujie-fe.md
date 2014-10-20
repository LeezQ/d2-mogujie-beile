title: 面向多端的蘑菇街前端技术架构
speaker: beile
transition: vertical3d
files: /js/demo.js,/css/demo.css

[slide]

# 面向多端的蘑菇街前端技术架构 

<small>author: 贝勒</small>  
<small>mail: beile@moguije.com</small> 

[slide]

# 团队介绍 {:&.flexbox.vleft}


[slide]
## 目前的技术架构
----
* Webdemo - 本地开发环境 {:&.moveIn}
    * Walkman - 前端自动化工具 {:&.moveIn}
    * Magpie - MOGU-FE 底层

* Lotus - 数据模拟系统

* JsBridge - js 与 App 开发环境


[slide]

## Webdemo

---
* What ?
    * 本地开发环境 {:&.moveIn}

* Why ?
    * svn 代码太庞大 {:&.moveIn}
    * 后端服务太多，本地环境太复杂

* How ?
    * Nginx + PHP (Kohana) {:&.moveIn}
    * git: submodule (pc、h5、pad、im ...)
    * FE 开发环境: require.js + less + magpie + lotus
        * 如何处理 less ，php lessc -> sourcemap {:&.moveIn}


[slide]
## Magpie
---
* What ?
    *  PC 牛郎 & H5 织女，如何在一起？ {:&.moveIn}

* Why ?
    * 团队合并，网站改版 {:&.moveIn}
    * H5、PC 各自的一套开发体系，学习成本 
    * 如何让 PC 能够无缝切换

* How ?
    * 蘑菇街底层 js，统一各端的开发模式 {:&.moveIn}
        * 全局变量：MoGu
        * amd 的开发模式：define, require
        * 类 backbone 的 mv* ： 
        * base.js 作为底层库共各项目使用：magpie.pc.js ， magpie.h5.js


[slide]
## Walkman
---
* What ?
    *  前端自动化构建工具 {:&.moveIn}

* Why ?
    * 能自动的事情不要手动去做 {:&.moveIn}
    * 开发效率 
    * 强大的 Grunt

* How ?
    * Grunt：流程构建 {:&.moveIn}
    * r.js：打包 js
    * lessc：打包 css
    * yo：脚手架


[slide]
## Lotus
---
* What ?
    *  数据模拟系统 {:&.moveIn}

* Why ?
    * webdemo 没有数据层 {:&.moveIn} 

* How ?
    * Mean.io {:&.moveIn}
    * 根据接口直接生成文档
    * 先定接口再开发

[slide]
## JsBridge
---
* What ?
    * 和 hybrid app 的开发环境 {:&.moveIn}



[slide]
## 目前的技术架构
----
* Webdemo - 本地开发环境 {:&.moveIn}
    * Magpie - MOGU-FE 底层
    * Walkman - 前端自动化工具

* Lotus - 数据模拟系统

* JsBridge - js 与 App 开发环境



[slide]
## 后  记
---
* 关于选型 {:&.moveIn}
    * 小而美，可替换
    * 拥抱开源

* 效率 
    * 视团队而定，视规模而定

* 前后端分离

* 面向全端、面向全栈 
    * 前端只是写前端的？

