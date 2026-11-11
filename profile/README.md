<p align="center"><img src="https://raw.githubusercontent.com/JianShanAgent/.github/main/profile/icon.svg" width="96" alt="JianShanAgent"></p>

# JianShanAgent（见山）

给 MediaWiki 站点用的 QQ 问答机器人，名字取自「开门见山」。核心只懂 MediaWiki 和 QQ；
某个 wiki 平台、某个站特有的东西由插件带进来；把它们拼起来指向某一个 wiki 的是实例。

JianShanAgent is a QQ question-answering bot for MediaWiki sites. The core knows only MediaWiki and QQ;
anything specific to a wiki platform or a single wiki comes in as a plugin, and an *instance* repository
pins the pieces together for one deployment. Documentation is in Chinese.

组织里不能给仓库分文件夹，仓库按名字前缀和话题标签分层，这里是按层排的目录。

## 核心

| 仓库 | 管什么 |
|---|---|
| [`agent-core`](https://github.com/JianShanAgent/agent-core) | 机器人本体：QQ 网关、七个功能插件、管理后台、部署工具。文档：[架构](https://github.com/JianShanAgent/agent-core/blob/main/docs/架构.md)、[插件规范](https://github.com/JianShanAgent/agent-core/blob/main/docs/插件规范.md)、[部署与运维](https://github.com/JianShanAgent/agent-core/blob/main/docs/部署与运维.md) |

## 站点插件

| 仓库 | 层 | 管什么 |
|---|---|---|
| [`site-huiji`](https://github.com/JianShanAgent/site-huiji) | 平台 | 灰机 wiki 平台 |
| [`site-huiji-yys`](https://github.com/JianShanAgent/site-huiji-yys) | 站（建在灰机上） | 阴阳师 wiki |

## 实例

| 仓库 | 管什么 |
|---|---|
| [`instance-yys`](https://github.com/JianShanAgent/instance-yys) | 阴阳师 wiki 的 QQ 机器人这个部署 |

## 模板

新建某一层的仓库时，从对应的模板复制（仓库页面上的「Use this template」）。

| 仓库 | 用来建什么 | 建出来的仓库叫什么 |
|---|---|---|
| [`template-site-platform`](https://github.com/JianShanAgent/template-site-platform) | 一个 wiki 平台的插件 | `site-<平台>` |
| [`template-site-wiki`](https://github.com/JianShanAgent/template-site-wiki) | 一个 wiki 的插件 | `site-<平台>-<站>`，不建在平台上的是 `site-<站>` |
| [`template-instance`](https://github.com/JianShanAgent/template-instance) | 一个部署 | `instance-<名字>` |

## 约定

- 命名、插件的目录和清单、怎么登记、文档的格式：见[插件规范](https://github.com/JianShanAgent/agent-core/blob/main/docs/插件规范.md)。
- 话题标签：每个仓库都有 `jianshanagent`、`mediawiki`、`qq-bot`，再按层有 `core`、`site-plugin`、`platform`、`instance`、`template`。
- 许可：MIT。
- 新建仓库以后，在这份目录里加一行。
