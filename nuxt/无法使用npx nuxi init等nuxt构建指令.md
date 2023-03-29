# **无法使用`npx nuxi init`等nuxt构建指令**

## **前述**

最近在家中构建一个nuxt初始模板，死活构建不下来，出现以下错误代码：

```bash
Error: Failed to download template from registry: fetch failed
```

一开始以为是代理有问题，设置了cmd的代理，设置了powershell的代理，设置了npm的代理，都无法解决问题。

但在公司的网络环境下可以正常拉取，通过对比发现可能是DNS的锅。

## **解决**

将DNS设置为`8.8.8.8`，备选`8.8.4.4`，发现可以正常拉取，且不需要开代理。而用默认的或`114.114.114.114`皆无法拉取，其他一些“冷门”`DNS`没有尝试，毕竟Google的DNS也够用了不是。

## **后言**

看来国内还是不够international啊！
