# “自我改进”实现调查

直接打开 `index.html`。页面完全离线，GitHub 外链固定到对应 commit。代码原样保存于 `code/`；代码块为节选；`source-manifest.json` 提供 SHA-256；`flowcharts.mmd` 是本次整理的 Mermaid 图源。

- 调查日期：2026-10-20
- Harness²：1cfe254e8d25b15f37048c3730134686abe60335
- Hermes-agent：0b10b9f8155a7ecadd8c540b87712c791b5c8ac9
- 范围：Harness² 任务内修改/执行/合成/选择/反思/跨题复用；Hermes 已有的后台技能与记忆学习路径。
- 未运行真实模型 benchmark，未运行 Hermes 学习流程。源码证明机制，不能证明效果。

## 复现已运行的演示

在原 Harness² 仓库根目录（Python 3.12 或 3.13）：

```sh
python3 -m harness2.cli.demo --output /tmp/harness2-self-improvement-demo --k 1 --mode both
```

`demo-run/` 是本次运行的关键记录；`demo-run-full.zip` 保存完整记录。上游 JSON 含原临时目录绝对路径，不作篡改；请按目录内的相对位置查看文件。

结果：2 tasks / 0 failed，14 次 Python 执行，16 次确定性编辑器调用；ledger-1：105.25 → 85.15；ledger-2：35.50 → 20.25。两模式共享基线。DemoProposer 的修复与反思是预先写好的，没有调用模型；第二题拿到经验，不代表证明了使用经验的因果收益。

代码副本保留上游许可证（Harness² Apache-2.0 / Hermes MIT）。解释与流程图为本次调查整理。
