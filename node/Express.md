# Express

#### express()

创建一个Express应用。express是模块入口函数

### 内置方法

#### express.static(root,[options])

express.static是内置唯一一个中间件。负责托管Express应用内的静态资源

```javascript
{
  dotfiles:'',//dot文件如 .git
  tag:'',//Etag 是URL的Entity Tag，用于标示URL对象是否改变，区分不同语言和Session等等。具体内部含义是使服务器控制的，就像Cookie那样。
  
}
```