## 1. WebStorge
HTML5 提供了两种在客户端存储数据的新方法,它包括localStorage和sessionStorage两种存储方式，均只保存字符串类型
### 1.1 localStorage
用于持久化的本地存储，浏览器窗口关闭后，localStorage存储的数据仍然可以被访问。所有浏览器窗口可以共享localStorage的数据，保存的数据永远不会过期，只能手动删除。
### 1.2 sessionStorage
用于本地存储一个会话中的数据，它不是一种持久化的本地存储。这些数据只有在同一个会话中的页面才能访问，当前页面不可以访问新开页面的数据，并且会话结束后数据也随之销毁而无法使用。

## 2. 用法
|方法|描述|
|:----|:----|
|getItem(key)|获取指定key本地存储的值|
|setItem(key, value)|将value值存储到本地的key字段|
|removeItem(key)|删除指定key本地存储的值|
|clear()|删除localStorage中存储的所有数据|
|length|获取存储的键值对的数量|
|key(index)|根据索引获取一个指定位置的键名|
 	
### 2.1 localStorage 
localStorage 方法存储的数据没有时间限制。第二天、第二周或下一年之后，数据依然可用
#### 2.1.1 如何创建和访问 localStorage：
```javascript
    localStorage.lastname="Smith";
    document.write(localStorage.lastname);
```

#### 2.1.2 对用户访问页面的次数进行计数
```javascript
if (localStorage.pagecount)
  {
  localStorage.pagecount=Number(localStorage.pagecount) +1;
  }
else
  {
  localStorage.pagecount=1;
  }
document.write("Visits "+ localStorage.pagecount + " time(s).");

```

### 2.2 sessionStorage 方法
sessionStorage 方法针对一个 session 进行数据存储。当用户关闭浏览器窗口后，数据会被删除。
#### 2.2.1 创建并访问一个 sessionStorage
```javascript
sessionStorage.lastname="Smith";
document.write(sessionStorage.lastname);
```

#### 2.2.2 对用户在当前 session 中访问页面的次数进行计数
```javascript
if (sessionStorage.pagecount)
  {
  sessionStorage.pagecount=Number(sessionStorage.pagecount) +1;
  }
else
  {
  sessionStorage.pagecount=1;
  }
document.write("Visits "+sessionStorage.pagecount+" time(s) this session.");

```

 	
 	
 	
 	

