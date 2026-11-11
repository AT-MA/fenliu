# 分流（fenliu）

自用的 Quantumult X 分流规则，每个文件通过 raw 链接被 `filter_remote` 订阅。

## 工作方式

- 改动不用先问我，直接改好、提交、开 PR 并合并到 main，做完告诉我结果就行
- 合并后检查一下 main 上的内容（比如 raw 链接）是否正确

## 规则约定

- 每行一条：`类型,值,策略`，逗号两边不留空格，类型小写（host / host-suffix / host-keyword / ip-cidr）
- 新建规则文件时，策略名用文件名（如 `Weex`）
- 不完整的域名（没有 .com 之类结尾）用 host-keyword，完整域名用 host-suffix
- 不要重命名已有的规则文件，否则订阅链接会失效
- 增删规则后同步更新 README.md 里的规则表（用途、规则数、订阅链接）
