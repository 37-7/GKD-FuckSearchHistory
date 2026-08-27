# GKD-FuckSearchHistory

> 自动清理 Android 应用搜索历史的 GKD 订阅。  
> A GKD subscription for automatically clearing search history in Android apps.

[中文](#中文) · [English](#english)

---

## 中文

### 简介

**GKD-FuckSearchHistory** 是一个面向 [GKD](https://github.com/gkd-kit/gkd) 的第三方订阅规则集，用于在你进入应用的**搜索页 / 历史记录页**后，自动执行清除搜索历史所需的点击操作。

本订阅**不会从 APP 首页自动导航到搜索页**；规则只会在对应页面和匹配条件出现时执行。

### 订阅

将下面的链接复制到 GKD 的订阅添加界面即可：

```text
https://raw.githubusercontent.com/37-7/GKD-FuckSearchHistory/main/gkd.json5
```

备用 jsDelivr 地址：

```text
https://fastly.jsdelivr.net/gh/37-7/GKD-FuckSearchHistory@main/gkd.json5
```

### 使用方法

1. 安装并配置 [GKD](https://github.com/gkd-kit/gkd)。
2. 打开 GKD → **订阅** → **添加订阅**。
3. 粘贴上面的订阅链接并添加。
4. 启用你需要的应用规则。
5. 正常进入目标应用的搜索页 / 搜索历史页，匹配成功后规则会自动执行清理流程。

### 当前覆盖

当前 JSON5 包含 **27 个应用**：

小红书、Hydrogen、PXVR、百度贴吧、柠檬音乐、网易云音乐、哔哩哔哩、微信、最右、微博、喜马拉雅极速版、夸克网盘、百度网盘、百度网盘国际版、酷安、QooApp、TapTap、软件商店、小米系统应用商店、AppShare、网易有道词典、金山文档、阿里云盘、美团、淘宝、闲鱼、拼多多。

其中，**夸克网盘**规则使用实验性坐标点击，因为对应 WebView 没有暴露可用的无障碍节点，因此默认关闭；仅建议在确认界面与规则适配后手动测试。

### 更新与反馈

GKD 只有在订阅文件中的 `version` 增大时才会执行订阅更新。因此发布规则更新时，请同时递增 `version`。

如果规则失效、应用 UI 改版或出现误触，欢迎通过 [Issues](https://github.com/37-7/GKD-FuckSearchHistory/issues) 提交反馈。若能附上 GKD 快照链接，会更方便定位问题。

### 说明

本项目仅提供 GKD 自动点击规则。应用更新可能导致节点、Activity、文案或页面结构变化，从而使规则失效。请按需启用规则，并自行确认自动清理搜索历史符合你的使用预期。

---

## English

### About

**GKD-FuckSearchHistory** is a third-party subscription for [GKD](https://github.com/gkd-kit/gkd). It automatically performs the taps required to clear search history after you enter a supported app's **search page / history page**.

This subscription **does not navigate from an app's home screen to its search page**. Rules only run when the corresponding page and matching conditions are detected.

### Subscription

Copy the following URL into GKD's subscription manager:

```text
https://raw.githubusercontent.com/37-7/GKD-FuckSearchHistory/main/gkd.json5
```

Alternative jsDelivr URL:

```text
https://fastly.jsdelivr.net/gh/37-7/GKD-FuckSearchHistory@main/gkd.json5
```

### Usage

1. Install and configure [GKD](https://github.com/gkd-kit/gkd).
2. Open GKD → **Subscriptions** → **Add subscription**.
3. Paste the subscription URL above.
4. Enable the rules for the apps you want to use.
5. Open the target app's search or search-history page. When the rule matches, GKD will automatically perform the cleanup sequence.

### Currently Covered

The current JSON5 contains rules for **27 apps**:

小红书, Hydrogen, PXVR, 百度贴吧, 柠檬音乐, 网易云音乐, 哔哩哔哩, 微信, 最右, 微博, 喜马拉雅极速版, 夸克网盘, 百度网盘, 百度网盘国际版, 酷安, QooApp, TapTap, 软件商店, 小米系统应用商店, AppShare, 网易有道词典, 金山文档, 阿里云盘, 美团, 淘宝, 闲鱼, 拼多多.

The **Quark Cloud Drive (夸克网盘)** rule uses experimental coordinate-based taps because the corresponding WebView does not expose usable accessibility nodes, so it is disabled by default. Enable it manually only after confirming that the target UI matches the rule. 

### Updates & Feedback

GKD only replaces an installed subscription when the new subscription's `version` is greater than the local version. When publishing rule updates, increment `version` as well.

If a rule stops working, an app changes its UI, or you encounter an accidental trigger, please open an [Issue](https://github.com/37-7/GKD-FuckSearchHistory/issues). Providing a GKD snapshot link will make debugging much easier.

### Notes

This repository only provides GKD automation rules. App updates may change accessibility nodes, Activity names, labels, or page structures and can therefore break existing rules. Enable only the rules you need and make sure automatic search-history cleanup matches your intended use.
