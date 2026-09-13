<p align="center">
	<img src="assets/logos/surgeshield-logo.png" alt="surgeshield logo" width="160">
</p>

<h1 align="center"><span style="font-family: 'Times New Roman', Times, serif;">surgeshield</span></h1>

<p align="center">面向 Surge iOS 与 macOS 的个人数字防火墙配置与规则集</p>

<p align="center">
	<a href="https://github.com/chentaoinbox/surgeshield"><img src="https://img.shields.io/github/license/chentaoinbox/surgeshield?label=license" alt="Apache-2.0 license"></a>
	<a href="https://github.com/chentaoinbox/surgeshield/commits/main"><img src="https://img.shields.io/github/last-commit/chentaoinbox/surgeshield" alt="Last commit"></a>
</p>

surgeshield 是基于 [Thoseyearsbrian/Aegis](https://github.com/Thoseyearsbrian/Aegis) 整理和维护的 Surge 配置仓库，用于对网络请求进行识别、分类、分流和防御性拦截。

> **来源声明**：本仓库源自上游项目 [Aegis: Personal Digital Firewall Ruleset for Surge on iOS & macOS](https://github.com/Thoseyearsbrian/Aegis)，原作者为 **ThoseYearsBrian**。surgeshield 是独立维护的派生仓库，不代表 Aegis 官方，也不构成上游作者的背书。

## 特性

- 支持 Surge iOS 与 macOS；
- 提供简体中文、繁体中文和英文配置；
- 同时提供 IPv4 与 IPv6 配置版本；
- 按广告、恶意软件、钓鱼、诈骗、后门、僵尸网络等风险类型组织拦截规则；
- 按 Apple、Google、Microsoft、GitHub、OpenAI、Telegram、微信、媒体和游戏平台等服务进行策略分组；
- 配置和规则文件保留注释，便于审阅、调整和持续维护。

## 快速使用

1. 在 Surge 中导入下列任一配置文件。
2. 根据自己的机场节点名称，修改 `policy-path` 或对应策略组。
3. 检查 DNS、IPv6、规则模块和 `FINAL,REJECT` 策略是否符合使用需求。

## 配置选择

| 配置文件 | 语言 | 网络协议 |
| --- | --- | --- |
| [Aegis_CN.conf](config/Aegis_CN.conf) | 简体中文 | IPv4 |
| [Aegis_TC.conf](config/Aegis_TC.conf) | 繁体中文 | IPv4 |
| [Aegis_EN.conf](config/Aegis_EN.conf) | English | IPv4 |
| [Aegis_IPv6_CN.conf](config/Aegis_IPv6_CN.conf) | 简体中文 | IPv6 |
| [Aegis_IPv6_TC.conf](config/Aegis_IPv6_TC.conf) | 繁体中文 | IPv6 |
| [Aegis_IPv6_EN.conf](config/Aegis_IPv6_EN.conf) | English | IPv6 |

## 目录结构

```text
config/   Surge 配置文件
rules/    按服务、地区和风险类型拆分的规则列表
assets/   Logo、图标和其他项目资源
docs/     上游项目的多语言说明文档
```

## 规则说明

规则模块默认按用途拆分。广告、成人内容、PCDN 和行为遥测模块在配置中默认注释；后门、僵尸网络、恶意软件 IOC、Pegasus、钓鱼、诈骗和风险通信模块默认启用。启用或调整规则前，请结合实际流量观察误拦截情况。

本项目用于防御性安全研究与个人网络管理，不能替代系统更新、终端防护或专业安全审计。

## 许可证与致谢

- 本仓库中的源自 Aegis 的内容遵循 [Apache-2.0](LICENSE)；
- Apache-2.0 要求再分发时保留许可证、版权和归属声明，并对修改过的文件作出说明；
- 第三方图片、图标、GeoIP 数据及外部规则资源可能适用各自的许可证或使用条款，请单独核查；
- 上游项目：[Thoseyearsbrian/Aegis](https://github.com/Thoseyearsbrian/Aegis)；
- 本仓库：[chentaoinbox/surgeshield](https://github.com/chentaoinbox/surgeshield)。