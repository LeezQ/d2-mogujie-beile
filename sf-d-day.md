title: 基于 React.js 的大规模网站开发实践
speaker: beile
transition: vertical3d
files: /js/demo.js,/css/demo.css

[slide]

# 基于 React.js 的大规模网站开发实践 

<small>author: 贝勒</small>  
<small>mail: beile@mogujie.com</small> 


[slide]

## 缘起

---
* 蘑菇街-小店 

  - ![](/publish/img/code.png)

  - ![](/publish/img/xiaodian01.png)


[slide]

### http://www.xiaodian.com 

---
![](/publish/img/xiaodian02.png)


[slide]

## 为什么选型 React ?

---
* Reactjs 是什么 ?
    * A JAVASCRIPT LIBRARY FOR BUILDING USER INTERFACES
    
    * ![](/publish/img/img.png) 


[slide]

## 为什么选型 React ?

---
* React Native
* 支持 IE8 



[slide]
## React
---
* 几个概念
    * component 组件 
    * state 和 props
    * Virtual Dom

* 看个例子



[slide]
## mogu-react-app-generator
----

* react
* webpack - 编译
* gulp - 前端自动化工具 

* Lotus - 数据模拟系统


[slide]
## 一些经验
----
* 双向绑定 
* mixin

```
    <input className="xd-input primary" type="password" valueLink={this.linkValue('pwd')} />
    linkValue: function(linkkey) {
        var data = {};
        return {
            value: this.state[linkkey],
            requestChange: function(newValue) {
                data[linkkey] = newValue;
                this.setState(data);
            }.bind(this)
        }
    }
```

[slide]
## 一些经验
----
* 数据传递 
    * leezq-react-model
    * pubsub-js
    * ES6 class
    * 封装了 save 等 ajax 方法，返回 promise

[slide]
## model
----
  - ![](/publish/img/model-demo.png)


[slide]
## model
----
  - ![](/publish/img/event-demo.png)


[slide]
## 总  结  
---
* React 带来的好处 
    * 组件化开发
    * 前后端代码层面的分离
    * 面向 ES6
    * React Native 的技术铺垫


