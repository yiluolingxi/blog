axios是一个基于Promise的HTTP库，可以用在浏览器和node.js中。它的主要特点包括：

1. 基于Promise：所有的请求都会返回Promise，这使得axios可以很好地与现代的JavaScript异步编程模式（如async/await）配合使用。
    
2. 支持拦截器：axios允许你在请求发送到服务器之前，或者在服务器响应到达客户端之前，对请求或响应进行修改。
    
3. 支持取消请求：axios提供了一种机制，可以在请求发送后，但在服务器响应到达之前，取消请求。
    
4. 自动转换JSON数据：当请求或响应的数据是JSON格式时，axios会自动将其转换为JavaScript对象。
    

axios的工作原理主要包括以下几个步骤：

1. 当你调用axios的方法（如get，post等）时，axios会创建一个新的请求。
    
2. 然后，axios会将请求配置与默认配置合并，并将合并后的配置应用到请求上。
    
3. 接着，请求会被添加到请求队列中。同时，请求拦截器会被调用。
    
4. 当请求拦截器完成后，请求会被发送到服务器。
    
5. 当服务器的响应到达时，响应拦截器会被调用。
    
6. 最后，响应会被返回给调用axios方法的代码。
    

这就是axios的基本原理。如果你想了解更多关于axios的细节，我建议你阅读axios的源码。