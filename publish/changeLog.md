### 改版内容

- App 内「关于」页、许可协议弹窗里的开源地址、Issues、Releases、常见问题链接全部改指向本仓库
- 修正应用内更新检查：原先读取的是上游版本号，下载链接还会拼成 `lx-music-mobile-v*.apk` 去拿上游安装包，现在只查本仓库、按 `WecarFlow-v*.apk` 下载
- README、FAQ、Issue 模板中的地址与分支名（`master`、`dev` 统一改成 `main`）改正

### 已知限制

本仓库当前为私有仓库，`raw.githubusercontent.com` 匿名访问取不到 `publish/version.json`，所以 App 内「检查更新」会提示无法检查更新（不会再误报上游版本）。把仓库改为公开后该功能即可正常使用。

### 安装包说明

- `arm64-v8a`：绝大多数车机、近年的手机，优先选这个
- `armeabi-v7a`：老的 32 位 ARM 设备
- `universal`：不确定设备架构时选这个，体积最大
- `x86` / `x86_64`：模拟器或部分车机

### 注意

本版本使用 Android 调试密钥签名，后续如更换正式签名密钥需卸载后重新安装。
