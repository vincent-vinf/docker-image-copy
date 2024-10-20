# docker-image-copy
使用Github Action将Docker镜像转存到阿里云镜像仓库。

* 支持docker hub、k8s.io、ghcr.io等仓库
* 支持多架构，默认拷贝全架构镜像。
* 支持任意大小的镜像，实测转存了50G的xxx镜像



## quickstart

### 准备配置

进入[阿里云容器镜像服务](https://cr.console.aliyun.com/)，选择个人版实例，点击仓库管理-命名空间，创建命名空间(**ALIYUN_NAME_SPACE**)

点击访问凭证，设置固定密码(**ALIYUN_REGISTRY_PASSWORD**)

![image-20241020151055734](assets/image-20241020151055734.png)

并在下方查看，用户名(**ALIYUN_REGISTRY_USER**)以及仓库地址(**ALIYUN_REGISTRY**)

### 配置github action

fork本项目，在你自己的项目中，点击settings-security-actions，将上述提到的4个secrets配置到项目中。

![image-20241020151642964](assets/image-20241020151642964.png)
