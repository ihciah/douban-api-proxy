# DouBan API Proxy

## 功能

替代 `api.douban.com` 用的代理服务，主要解决电影搜索接口下架的问题，[配合这个 Alfred 扩展使用](https://github.com/lucifr/Alfredv2-Extensions/blob/master/Douban.alfredworkflow)。

对于电影搜索 API ，本服务会模拟浏览器调用搜索接口并尽量提供成原有电影搜索接口的格式；对于其他接口，本服务直接透明代理掉。

## 部署

本服务部署于 Cloudflare Workers 。配置好环境后，修改 `wrangler.toml` 中的配置（ `account_id` 和 `name` ），然后 `wrangler publish` 即可。

懒得配置环境直接将 `index.js` 复制粘贴在在线编辑器中。

使用时直接替换原有域名。

## 声明

本代码中的豆瓣数据解密代码取自 [SergioJune/Spider-Crack-JS](https://github.com/SergioJune/Spider-Crack-JS)。
