# youtube-noads-clean

Shadowrocket 用 YouTube 去广告脚本（清洗版），供个人使用。

## 文件
- `youtube_noads_clean.js` — 基于 Maasea 的 `youtube.response.js` 修改

## 清洗内容
- 删除了把画中画 / 后台播放能力伪造成已开启的代码
- 删除了往设置里塞入后台播放 / 下载已开启条目的代码
- 删除了模块原有的 ctier 请求篡改规则（在配套模块中处理）
- 只保留：在本地删除已收到的响应里的广告数据（片头广告位、信息流和 Shorts 广告条目）
- 不修改任何发往服务器的请求，不向服务器回传伪造数据

## 使用
本仓库为 **公开（Public）** 仓库，脚本的长期直链是：

`https://raw.githubusercontent.com/xi-zhi185/youtube-noads-clean/main/youtube_noads_clean.js`

把配套 Shadowrocket 模块里的 `script-path=` 换成上面这个地址即可。也可经 jsDelivr 拉取同一文件：
`https://cdn.jsdelivr.net/gh/xi-zhi185/youtube-noads-clean@main/youtube_noads_clean.js`

## 验证
2026-11-13 在真机 Shadowrocket 上验证：片头和信息流广告均已去除。
