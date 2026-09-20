# 落雨秋远程接口

这是给“落雨秋”播放器使用的远程配置，完整保留自当前可用接口的 JSON 配置。

播放器配置地址：

```text
https://raw.githubusercontent.com/jokers963/luoyuqiu-api/main/config.json
```

如果 GitHub Pages 已启用，也可以使用：

```text
https://jokers963.github.io/luoyuqiu-api/config.json
```

## 当前状态

- `config.json` 已保留站点、解析器、直播、规则和其他配置。
- JSON 中原有的 `spider` 地址已保留。
- 原 `spider` 地址当前返回 404，因此依赖其中自定义 `Guard` 类的站点，需要替换为有效且有授权的 Spider JAR 后才能完整恢复。

仓库是公开的，因为播放器需要无需登录即可读取配置。配置内的上游地址和参数也会随仓库公开，请仅保留你有权使用的内容。
