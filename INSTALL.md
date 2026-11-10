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

## Windows 免安装包

1. 从 [最新 Release](https://github.com/chengzi-06/mirai-nihongo-monogatari-releases/releases/latest) 或更新页下载 `MiraiNihongoMonogatari-*-windows.zip`（当前为 `MiraiNihongoMonogatari-2026.11.09d-windows.zip`）
2. 解压整个文件夹，不要只抽出 exe
3. 双击 `KyoanJapanese.exe`（也可双击 `start.bat` 或 `启动.bat`）
4. 若 Windows SmartScreen 提示「已保护你的电脑」，点「更多信息」→「仍要运行」
5. 不需要安装 Python、Node 或 Chrome。学习记录保存在 `%APPDATA%\KyoanJapanese`，覆盖文件夹升级一般会保留

建议校验（PowerShell）：

```powershell
Get-FileHash -Algorithm SHA256 MiraiNihongoMonogatari-2026.11.09d-windows.zip
# 应为 8e562710ec3029c2862db60cf0b2d1d14cc0e5ef1e32bbd666e7447fd33c2c5e
```

## Web / 浏览器版（PWA）

当前版本尚未提供独立 Web zip。请使用 macOS App 或 Windows 免安装包，或等待后续清单中的 `assets.web`。

## 学习记录

- macOS / 浏览器：进度与设置保存在浏览器 **localStorage**。覆盖安装一般会保留；换浏览器、清站点数据或换机器会丢失。
- Windows 包：学习记录在 `%APPDATA%\KyoanJapanese`。覆盖解压目录升级一般不会清除该目录。

## 注意

- 升级前请先关闭旧版，避免文件占用
- 软件内「检查 GitHub 更新」只会打开下载页，**不会自动替换**本地 App
