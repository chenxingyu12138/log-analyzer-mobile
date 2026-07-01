# 日志分析助手 Mobile

这是纯前端版本，不需要后端服务器。用户在手机浏览器里选择 `.log` 文件后，浏览器会在本地完成：

- 日志二进制解析
- CSV 生成和下载
- 图表展示
- 图表 PNG 下载

数据不会上传到服务器。

## 分发方式

把 `mobile_static` 整个目录上传到任意静态网站即可，例如：

- 阿里云 OSS 静态网站
- 腾讯云 COS 静态网站
- GitHub Pages
- 公司已有网站目录
- 内网静态文件服务器

入口文件是：

```text
index.html
```

必须同时保留：

```text
plotly.min.js
manifest.webmanifest
sw.js
```

## 本地测试

直接双击 `index.html` 通常可以使用。若要测试 PWA 缓存，请在项目根目录运行：

```bash
python -m http.server 8080 -d mobile_static
```

然后访问：

```text
http://127.0.0.1:8080
```
