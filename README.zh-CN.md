# RippleGL — 光子学探索 fork

**[Paul Falstad 的 RippleGL](https://github.com/pfalstad/ripplegl) 光子学取向分支。** 上游提供 Java／GWT 浏览器波纹槽与 WebGL 基础；本 fork 探索附加介质、源与电磁表述。

[English](README.md) · [上游模拟器](https://www.falstad.com/ripple/) · [源码历史](docs/README-history.md)

## 实际差异

公开版本 `3be54cd` 包含光子晶体对象、椭圆光子晶体变体、时变介质、阻尼／PML 实验、附加示例及 WebGL 模拟改动。最后的历史提交称 **TE 电磁 FDTD 方法仍在测试**，提交描述本身不是准确度基准。

**2026-10-17** 核对时，公开 fork 相对上游 `master`（`f8ddee1`）为 **领先 30、落后 1 个提交**。[固定版本对照](https://github.com/pfalstad/ripplegl/compare/f8ddee15806a27be68f002c0c4bfcf0997029e50...Patr1ck2005:3be54cd5fe54c4f4d0a5c539024f821a004b6a5c) 保留归属和实际差异文件。

| 源码 | 内容 |
|---|---|
| [src/com/falstad/ripple/client/](src/com/falstad/ripple/client/) | Java／GWT 界面与模拟对象 |
| `PhotonicCrystal.java`、`PhotonicCrystalEllipse.java` | 上述目录内的 fork 光子晶体对象 |
| `TimeCrystalMediumBox.java`、`PMLLayer.java` | 时变介质及边界实验 |
| `war/Ripple.html`、`war/ripple.js` | 页面与 WebGL 侧实现 |
| [src/com/falstad/ripple/public/examples/](src/com/falstad/ripple/public/examples/) | 已有示例配置 |
| [app/](app/) | 历史 Electron 外壳 |

## 构建与体验

[上游在线模拟器](https://www.falstad.com/ripple/) 展示的是**上游 RippleGL**，不包含本 fork 专属改动。本页不宣称另有已经验证的 fork 在线版本。

原构建采用 Eclipse Java 环境与 GWT 插件：导入工程，运行 GWT 开发模式，或通过 **GWT Compile Project** 输出到 `war/`，再提供编译后的目录并打开 `Ripple.html`。详细旧步骤见 [原 README](docs/README-history.md)。Electron 外壳也需要 GWT 编译产物，其旧依赖不是当前持续维护的桌面发行版。

## 科学与维护状态

这是历史探索分支。定量科研使用前，附加介质、阻尼／PML 及电磁代码需要分别核验稳定性、色散、边界反射和收敛；示例名称与提交信息不证明已验证。本次未重建旧工具链、运行仿真或发布新科研结果。本机其他重写不属于此公开 fork 的能力声明。

## 许可与致谢

RippleGL 的原版权与作者归属 **Paul Falstad 及上游贡献者**，GWT 移植脉络同时致谢 Iain Sharp。原 README 和源码头声明 **GNU GPL 第 2 版或后续版本**，见 [源码头](src/com/falstad/ripple/client/RippleSim.java) 与 [GNU GPL v2 正文](https://www.gnu.org/licenses/old-licenses/gpl-2.0.html)。本 fork 不替换为 MIT；Electron 等组件分别适用自身条款。
