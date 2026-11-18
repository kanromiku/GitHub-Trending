# github-trending

`@morehao/dsh-github-trending` 插件的归档数据仓库。

插件按日 / 周 / 月周期调用本地 `trendradar` 核心抓取 GitHub Trending，生成中文榜单与周期总结，写入本仓库的 `trending/` 目录并提交；`commitMode: branch` 时另起分支并开 PR 合并。

## 目录约定

- `trending/` —— 榜单正文，按周期与日期分文件（`output.dir` 配置项，相对仓库路径）
- 订阅清单也随本仓库版本化，可与榜单一起审计

## 注意

- 插件只检查「目录存在 + `.git` 存在」，不会替你做 `git init`
- 推送与开 PR 需要可写的远端（`origin`）与 GitHub 凭据
- 本仓库只存数据，不放代码
