# GeoPing

一个纯前端节点地区与参考速度检测网页。

GeoPing 用于检测当前 IP 出口地区、系统环境与节点参考速度，适合在切换 VPN、代理或机场节点后，快速确认当前网络出口是否连接到目标地区。

## 功能

- 检测当前公网 IP
- 显示节点所在国家和地区代码
- 中文显示国家名称
- 显示浏览器语言
- 显示系统时区
- 显示节点时区
- 判断系统时区与节点时区是否接近
- 进行参考测速
  - 延迟 5 次采样，取中位数
  - 下载 5MB × 2 轮，取平均速度
- 可选显示 ASN、运营商或 ISP 信息

## 使用场景

- 切换节点后确认出口地区
- 简单判断节点速度是否异常
- 检查浏览器语言、系统时区与节点地区是否一致
- 作为 GitHub Pages 静态网页工具使用

## 部署方式

将 `index.html` 上传到 GitHub 仓库根目录，然后开启 GitHub Pages。

GitHub Pages 设置路径：

```text
Settings → Pages → Deploy from a branch → main → /root → Save
```

部署完成后访问：

```text
https://guguli685-creator.github.io/geoping/
```

## 说明

GeoPing 是纯前端工具，不需要后端服务器。

测速结果受浏览器、代理线路、Cloudflare 节点、移动网络策略和当前网络环境影响，只适合作为参考，不等同于专业测速软件结果。

ASN、运营商、ISP 等高级信息依赖公开接口，能获取时会自动显示，获取不到时会隐藏。

## 项目定位

GeoPing 专注于轻量检测：

```text
出口地区
系统环境
参考速度
```

它不做节点纯净度、VPN 识别、Proxy 识别、Tor 识别、滥用记录或账号风控判断。

## License

MIT
