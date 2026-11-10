# 安装与升级

## macOS App

1. 从 [最新 Release](https://github.com/chengzi-06/mirai-nihongo-monogatari-releases/releases/latest) 或更新页给出的链接下载 `MiraiNihongoMonogatari-*-macos.zip`（当前为 `MiraiNihongoMonogatari-2026.11.09d-macos.zip`）
2. 解压得到 `未来中学日语物语.app`
3. 关闭正在运行的旧版
4. 将新 `.app` 拖到 `/Applications` 或 `~/Applications`（或原来的位置）覆盖
5. 首次打开若被拦截：系统设置 → 隐私与安全性 → 仍要打开；或在终端对 App 目录执行 adhoc 签名后重试

建议校验：

```bash
shasum -a 256 MiraiNihongoMonogatari-2026.11.09d-macos.zip
# 应为 c19c1c795b42c6738a2d567679b41fabdfb815e5deaee7939856b7109e4c2005
```

## Web / 浏览器版（PWA）

当前版本尚未提供独立 Web zip。可用本机已安装的 macOS App，或等待后续清单中的 `assets.web`。

## 学习记录

进度与设置保存在浏览器 **localStorage**。覆盖安装一般会保留；换浏览器、清站点数据或换机器会丢失。升级前不必导出，除非你要迁移到另一台设备。

## 注意

- 升级前请先关闭旧版，避免文件占用
- 软件内「检查 GitHub 更新」只会打开下载页，**不会自动替换**本地 App
