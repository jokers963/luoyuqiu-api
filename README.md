# 落雨秋远程接口

这是给“落雨秋”播放器使用的远程配置和 Spider 资源。

仓库同时保留两套入口：

- `jsm.json`：配套 `pg.jar`、`js/` 和 `lib/` 的完整资源包，当前唯一推荐用于实际测试。
- `config-pg.json`：基于 `pg.jar` 的精简远程配置，只保留依赖文件齐全的站点。
- `config.json`：从原接口保存的完整配置快照。
- `config-like.json`：仅用于保留原接口的 63 个站点显示和配置结构；原接口的 `Wex...Guard` 类不在 `pg.jar` 中，不保证可运行。

## 推荐入口

```text
https://jokers963.github.io/luoyuqiu-api/jsm.json
```

如果希望优先看到与原接口接近的站点列表，可以测试：

```text
https://jokers963.github.io/luoyuqiu-api/config-like.json
```

`jsm.json` 使用本仓库的 `pg.jar`，并通过相对路径加载同目录下的 `js/` 和 `lib/`，因此这些文件必须保持现有目录结构。

直接配置地址：

```text
https://jokers963.github.io/luoyuqiu-api/config-pg.json
```

原配置快照地址：

```text
https://raw.githubusercontent.com/jokers963/luoyuqiu-api/main/config.json
```

原配置快照的 Pages 地址：

```text
https://jokers963.github.io/luoyuqiu-api/config.json
```

## 当前状态

- `config.json` 已保留原接口的站点、解析器、直播、规则和其他配置。
- `config-like.json` 保留原接口的 63 个站点和显示顺序，但其中依赖原专用 `Guard` 类的站点不保证可用。
- `pg.jar` 的 MD5 已与 `pg.jar.md5` 校验一致。
- `jsm.json`、`pg.jar`、`js/` 和 `lib/` 已按相对路径放置。
- 原 `config.json` 中的旧 `spider` 地址当前返回 404；新资源包使用本仓库内的 `pg.jar`。

仓库是公开的，因为播放器需要无需登录即可读取配置。配置内的上游地址和参数也会随仓库公开，请仅保留你有权使用的内容。
