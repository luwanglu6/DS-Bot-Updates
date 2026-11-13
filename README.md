# DS Bot Updates

Public distribution channel for DS Bot updates. Application source, credentials, signing configuration and runtime data are not stored in this repository.

- Update pages: https://luwanglu6.github.io/DS-Bot-Updates/
- HarmonyOS channel: https://luwanglu6.github.io/DS-Bot-Updates/harmony/
- Signed packages: https://github.com/luwanglu6/DS-Bot-Updates/releases
- Reserved HarmonyOS feed: https://luwanglu6.github.io/DS-Bot-Updates/harmony/latest.json

The initial setup publishes information pages only. The version feed intentionally remains absent until a signed release has been verified and published. A missing feed is not an available update.

## Publishing

The initial deployment workflow is manual. GitHub Pages is not enabled yet; enablement requires a separate approval before running that workflow. The first signed-release export supplies the automatic Pages workflow.

Upload and verify the signed HAP and its SHA256 in a Release before publishing pages that announce it. Commit generated update pages and manifests under `site/`; the Pages workflow deploys only that directory. Do not commit HAP packages, private keys, provisioning profiles, source checkouts or local runtime data to `site/`.

GitHub hosting does not bypass HarmonyOS signature, device authorization or installation requirements. Downloading a package or opening a page does not mean that an update has been installed.

## 中文

此仓库仅用于公开分发更新文件，不存放应用源码、凭据、签名配置或运行数据。首次初始化只发布说明页；经过验证的签名包发布之前，不创建 `latest.json`，也不宣告存在可安装的新版本。

签名安装包及校验值先上传至 Releases，确认完整后再更新 `site/` 中的页面和清单，由 GitHub Actions 自动发布 Pages。GitHub 托管不能绕过鸿蒙签名、设备授权或系统安装要求。

The public channel configuration and original information pages are provided under Apache-2.0; individual release packages retain their own notices and license terms.
