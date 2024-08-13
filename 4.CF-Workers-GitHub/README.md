# CF-Workers-GitHub 加速

这个项目是一个基于 Cloudflare Workers 的 GitHub 代理工具。

## 部署方式

首页：[https://workers.cloudflare.com](https://workers.cloudflare.com/)

- **Workers** 部署：复制 [_worker.js](https://github.com/iCloudBot/DockerRescue/blob/main/4.CF-Workers-GitHub/worker.js) 代码，`保存并部署`即可
- **Pages** 部署：`Fork` 后 `连接GitHub` 一键部署即可

`ASSET_URL` 是静态资源的url（实际上就是现在显示出来的那个输入框单页面）

`PREFIX`是前缀，默认（根路径情况为"/"），如果自定义路由为 example.com/gh/*，请将PREFIX改为 '/gh/'，注意，少一个杠都会错！

## 如何使用？

例如：您的Workers项目域名为：`https://gh.gtihub.io/`；github项目地址：`https://github.com/iCloudBot/DockerRescue.git`

```shell
git clone https://gh.gtihub.io/https://github.com/iCloudBot/DockerRescue.git
```


## 捐赠

|                    微信                    |                   支付宝                    |
| :--------------------------------------: | :--------------------------------------: |
| ![wx](../2.Deploy-Docker-Proxy/docs/imgsrc/wx.png) | ![wx](../2.Deploy-Docker-Proxy/docs/imgsrc/zfb.png) |

