
## 按照与启动

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

## 依赖模块说明

1. http模块使用 雷神thor

## thor使用说明
引用
```
import thor from '../../common/thor/thor'
```
以下方法config参照[wx.request](https://developers.weixin.qq.com/miniprogram/dev/api/network-request.html#wxrequestobject)

get, delete等 请求
```
  thor.get(url,config)
    .then(res=>{
      console.log('请求成功', res);
    })
    .catch(err=>{
      console.log('请求失败',err);
    })

```
post,put,patch等请求
```
thor.post(url,data,config)
    .then(res=>{
      console.log('请求成功', res);
    })
    .catch(err=>{
      console.log('请求失败',err);
    })
```

通用请求
```
thor.request({
        url:'',//地址
        method:'',//方法
        data:''//参数
        header:'' //有需要就填
    })
    .then(res=>{
      console.log('请求成功', res);
    })
    .catch(err=>{
      console.log('请求失败',err);
    })
```
