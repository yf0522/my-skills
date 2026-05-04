# my-skills

我的 AI agent Skill 个人库。由 [skill-sync](https://github.com/yf0522/skill-sync) 管理：每个子目录是一个 Skill（包含 `SKILL.md`），通过软链接被 Claude Code / Codex CLI / Cursor 调用。

## 在新机器上还原

```bash
# 1. 装 skill-sync 工具
git clone git@github.com:yf0522/skill-sync.git ~/workSpace/skill-sync
cd ~/workSpace/skill-sync && npm link

# 2. 把这个 my-skills 仓 clone 到 ~/.skill-sync/skills
mkdir -p ~/.skill-sync
git clone <THIS_REPO> ~/.skill-sync/skills

# 3. 生成本地 config，把所有 skill 链接到三家工具
skill-sync init
skill-sync repair
```

## 日常操作

```bash
skill-sync add  <name>      # 新建 skill 并自动链到三家
skill-sync edit <name>      # 改一处，三家都生效
skill-sync list             # 看现状
git add . && git commit -m "..." && git push   # 备份这次改动
```
