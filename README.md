# Cloudgo-io
设计一个web小应用，展示静态文件服务、js请求支持、模板输出、表单处理、Filter中间件设计等能力。

## 使用示范
1. 运行
`$go run main.go`
`[negroni] listening on :8080`

2. 访问home/date
![](https://github.com/moandy/cloudgo-io/blob/master/pictures/picture1.png?raw=true)

3. 访问静态文件
![](https://github.com/moandy/cloudgo-io/blob/master/pictures/picture3.png?raw=true)
![](https://github.com/moandy/cloudgo-io/blob/master/pictures/picture4.png?raw=true)
![](https://github.com/moandy/cloudgo-io/blob/master/pictures/picture5.png?raw=true)

4. js和html访问和表单提交，输出

![](https://github.com/moandy/cloudgo-io/blob/master/pictures/picture6.png?raw=true)
![](https://github.com/moandy/cloudgo-io/blob/master/pictures/picture7.png?raw=true)

5. 对 /unknown 给出开发中的提示，返回码501
![](https://github.com/moandy/cloudgo-io/blob/master/pictures/picture2.png?raw=true)

6. 客服端的返回数据
```
[negroni] listening on :8080
[negroni] 2017-11-21T22:03:07+08:00 | 200 |      469.879µs | localhost:8080 | GET /home/date
[negroni] 2017-11-21T22:05:42+08:00 | 404 |      100.021µs | localhost:8080 | GET /unkown
[negroni] 2017-11-21T22:05:55+08:00 | 501 |      64.492µs | localhost:8080 | GET /unknown
[negroni] 2017-11-21T22:06:37+08:00 | 304 |      85.884µs | localhost:8080 | GET /js/
[negroni] 2017-11-21T22:06:59+08:00 | 304 |      113.63µs | localhost:8080 | GET /css/
[negroni] 2017-11-21T22:07:23+08:00 | 200 |      127.515µs | localhost:8080 | GET /images/
[negroni] 2017-11-21T22:08:10+08:00 | 200 |      169.395µs | localhost:8080 | POST /
```