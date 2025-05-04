# mkdocs-toolchain

> My personal mkdocs toolchain, only for personal use.

我个人使用的 mkdocs 工具链，仅供个人使用、学习参考。

## 原创插件
自己写着玩的，可能有 bug，不过欢迎使用！

- [TonyCrane/mkdocs-changelog-plugin](https://github.com/TonyCrane/mkdocs-changelog-plugin)
- [TonyCrane/mkdocs-heti-plugin](https://github.com/TonyCrane/mkdocs-heti-plugin)
- [TonyCrane/mkdocs-statistics-plugin](https://github.com/TonyCrane/mkdocs-statistics-plugin)

未单独发布插件：

- mkdocs-linkbackward-plugin: 为了链接兼容性创建跳转页面
- mkdocs-tikzautomata-plugin: 在 markdown 中直接编写 tikz 并嵌入 svg，修改自 [FrightenedFoxCN/mkdocs-mathenv-plugin](https://github.com/FrightenedFoxCN/mkdocs-mathenv-plugin/)
- mkdocs-toc-plugin: 从页面内嵌 yml 生成 toc（带字数统计/更新时间）

## 各包原始 commit sha

- mkdocs: [`b7e8b62185b11d9f59bb7f50b13c15134f62f8a`](https://github.com/mkdocs/mkdocs/commit/bb7e8b62185b11d9f59bb7f50b13c15134f62f8a)
- mkdocs-encryptcontent-plugin: [`c28e4ce359cc3e69e097db8eba3fb77ab683b40d`](https://github.com/CoinK0in/mkdocs-encryptcontent-plugin/tree/c28e4ce359cc3e69e097db8eba3fb77ab683b40d)
- mkdocs-git-revision-date-localized-plugin: [`9cfce40942c83dd15834fb879caa4171a426ecdd`](https://github.com/timvink/mkdocs-git-revision-date-localized-plugin/tree/9cfce40942c83dd15834fb879caa4171a426ecdd)
- mkdocs-rss-plugin: [`89e9cfa8262e9b40f571d554a75a2e9929264efc`](https://github.com/Guts/mkdocs-rss-plugin/commit/89e9cfa8262e9b40f571d554a75a2e9929264efc)
- mkdocs-material: 不在此 repo 中，直接使用 9.6.5 版本（mkdocs-material-extensions 1.3.1）
- mkdocs-glightbox: 不在此 repo 中，直接使用 0.4.0 版本

## 各包做的修改
### mkdocs

- serve 模式下不监控 .DS_Store 文件（[`b13af4`](https://github.com/Jimmy-Bots/mkdocs-toolchain/commit/b13af45904917ab06eca446df54d6ac7e7548022)）

### mkdocs-encryptcontent-plugin
- 将一些 info 级别的无关紧要 log 降低为 debug 级别（[`751ff1`](https://github.com/TonyCrane/mkdocs-toolchain/commit/751ff15bfa549141b518059b260802c082b4a6f1)）
- 从加密页面中获取 summary、placeholder、encryption_info_message，而不是全部使用全局（[`59211c`](https://github.com/TonyCrane/mkdocs-toolchain/commit/59211cd433a9f4c88bf7e21a9c62c5e96a10d754)）
- 修复 toc 无法正常解密的 bug ([`648ac7`](https://github.com/Jimmy-Bots/mkdocs-toolchain/commit/648ac7971aa5ba27286bfee0e877f90c47ce8dda))

### mkdocs-git-revision-date-localized-plugin
- 在 serve 模式下自动关闭插件，加速预览（[`d90259`](https://github.com/TonyCrane/mkdocs-toolchain/commit/d902594c21d40b617ab203a531e1bbb83fd676b7)）

### mkdocs-rss-plugin
- 在 serve 模式下自动关闭插件，加速预览（[`ef7f45`](https://github.com/TonyCrane/mkdocs-toolchain/commit/ef7f45953d3b5d50e1eff282dc2ad37be014aa97)）
- 规范地使用 logger（[`ef7f45`](https://github.com/TonyCrane/mkdocs-toolchain/commit/ef7f45953d3b5d50e1eff282dc2ad37be014aa97)）