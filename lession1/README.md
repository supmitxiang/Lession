# Lession 1

## 设计模式

### 单例模式

* 概念
> 保证一个类只有一个实例，实现方法是先判断实例存在与否，如果存在直接返回，如果不存在就创建了再返回，确保一个类只有一个实例对象。在 JavaScript 中，单例作为一个命名空间提供者，从全局命名空间里提供一个唯一的访问点来访问该对象。

```
  var Single = (function(){
    var instance;
    /*这里定义单例代码*/
    var Init = function(){
      return {
        publicMethod: function(){
          console.log('hello world')
        },
        publicProperty: {
          test: 'test'
        }
      }
    }
    return {
      getIntance: function(){
        if(!instance){ //确保只有一个实例
          instance = init() //使用init方法，是使publicMethod和publicProperty只在要使用的时候才初始化
        }
        return instance
      }
    }
  })();
  /*调用公有的方法来获取实例:*/
  Single.getIntance().publicMethod() //hello world
```

