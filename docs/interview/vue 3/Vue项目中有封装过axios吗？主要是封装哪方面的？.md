在Vue项目中，我们通常会封装axios来进行HTTP请求。主要封装的方面包括：

1. 基础配置：例如，设置基础的URL，设置超时时间等。
    
2. 拦截器：axios提供了请求拦截器和响应拦截器。我们可以在请求拦截器中添加公共的请求头，处理请求参数等；在响应拦截器中，我们可以处理返回数据，处理错误等。
    
3. 错误处理：我们可以封装一个统一处理错误的函数，当请求出错时，我们可以在这个函数中处理错误。
    
4. 封装API：我们可以为每个API封装一个函数，这样在使用API时，我们只需要调用这个函数，而不需要关心具体的URL，请求方法等。
    

例如，一个基础的axios封装可能如下：
```js
import axios from 'axios';

const service = axios.create({
  baseURL: process.env.VUE_APP_BASE_API,
  timeout: 5000
});

service.interceptors.request.use(
  config => {
    // 在这里添加请求头，处理请求参数等
    return config;
  },
  error => {
    console.log(error);
    return Promise.reject(error);
  }
);

service.interceptors.response.use(
  response => {
    // 在这里处理返回数据
    return response.data;
  },
  error => {
    console.log('err' + error);
    return Promise.reject(error);
  }
);

export default service;
```
然后，我们可以为每个API创建一个函数：  
```js
import request from './request';

export function getUserInfo(userId) {
  return request({
    url: `/user/${userId}`,
    method: 'get'
  });
}
```
这样在使用API时，我们只需要调用这个函数即可