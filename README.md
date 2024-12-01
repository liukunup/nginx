# NGINX

- [NGINX](https://nginx.org/) 官方网站

- [NGINX Documentation](https://nginx.org/en/docs/)

- [NGINX Config](https://nginxconfig.io/) 是一个辅助配置工具

- [Tengine](https://tengine.taobao.org/) 由淘宝发起的Web服务器项目

## 使用说明

1. 从主分支拉出需求分支；

2. 修改分支里config配置，做好业务参数的配置；

3. 推送构建；

本地构建

```shell
# 构建
docker build -t liukunup/nginx:<version> .
# 推送
docker push liukunup/nginx:<version>
```

4. 一键拉起；

```Shell
docker run -d -p 80:80 --name=nginx liukunup/nginx:<version>
```

## 快速入门

- 反向代理 - [NGINX Reverse Proxy](https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/)

```
location /some/path/ {
    proxy_pass http://www.example.com/link/;
}
```
