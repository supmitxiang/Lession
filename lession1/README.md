# Lession 1



## 设计模式

# 单例模式

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