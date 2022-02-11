# 前端部署

### 静态资源组织

> 前端资源由HTML、Javascript、Css三剑客组成。
>
> + 利用缓存
>
> 浏览器缓存 ：Brower Caching是浏览器对之前请求过的文件进行缓存，在HTTp协议上定制了多种缓存策略。
>
> + 协商缓存
>
> 协商缓存：向服务器发送请求，根据 Request Header的参数判断是否命中协商缓存。
>
> + 强缓存
>
> 强缓存：浏览器不会向服务器发送任何请求，直接从本地缓存中读取文件并返回Status Code： 200 OK。

### 缓存更新问题

> - query-hash（消息摘要算法）更新URL，实现控制缓存。
>   `<link ref="stylesheet" href="boo.css?v=123234">`
> - name-hansh 方式解决HTML与Css的渲染版本出现缓存错乱。
>   `<link ref="stylesheet" href="boo.123234.css">`
>   先部署静态资源，再灰度部署页面。

### CDN结合

> CDN：一种内容分布网络 ，部署在应用层，利用智能分配技术，根据用户访问的地点，按照就近访问的原则分配到多个节点，来实现多点负载均衡。
>
> - 将 静态资源部署到CDN上，再将Nginx上的流量转发到CDN上，反向代理。

### 解决方案

- HTML设置为协商缓存，Js、Css等静态资源设置为永久强缓存。

- 为了解决强缓存更新问题，将文件摘要（hash）作为资源路径（URL）构成的一部分。

- 为了解决覆盖式发布引发的问题，采用name-hash而非query-hash的组织方式。`具体webpack配置：output.filename= contenthash`。

- 为了解决Nginx目录存储过大，结合CDN提升访问速度，采用Nginx反向代理+静态资源上传CDN。

  