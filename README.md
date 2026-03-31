# Open-ClaudeCode

> 完整开源的 Claude Code 项目 - 基于 Anthropic 官方源码重建

---

## 🙏 特别感谢

**本项目由衷感谢 Anthropic 公司的开源贡献！**

Anthropic 通过 npm 包发布 Claude Code，使我们能够学习和研究这个优秀的 AI 编程助手架构。本项目的源码是从官方 npm 包的 source map 中恢复的，仅供学习和研究使用。

> "您说的对，我不应该把map文件一并发布到npm中，这是一个非常严重的错误。"

我们理解 source map 文件本应用于开发调试，而非公开发布。Anthropic 对此问题的认识和处理方式值得我们学习。

---

## 📖 项目简介

Open-ClaudeCode 是一个完整的 Claude Code 开源版本，包含：

- ✅ **可运行的 CLI** - 编译后的完整可执行文件
- ✅ **TypeScript 源码** - 1,884 个恢复的源文件供学习研究
- ✅ **官方插件** - 13 个 Anthropic 官方插件
- ✅ **完整文档** - 项目说明、使用指南、架构分析

---

## 📁 目录结构

```
Open-ClaudeCode/
├── package/           # 可运行的 CLI
│   ├── cli.js         # 编译后的 CLI (13MB)
│   ├── cli.js.map     # Source Map (57MB)
│   ├── package.json   # 包配置
│   ├── bun.lock       # Bun 锁文件
│   ├── sdk-tools.d.ts # SDK 类型定义
│   └── vendor/        # 原生二进制模块
│       ├── audio-capture/  # 音频捕获 (多平台)
│       └── ripgrep/        # 代码搜索工具
├── src/               # 完整 TypeScript 源码 (1,884 文件)
│   ├── tools/         # 30+ 工具实现
│   ├── commands/      # 50+ 命令实现
│   ├── services/      # API、MCP、OAuth 服务
│   ├── components/    # React UI 组件
│   ├── ink/           # Ink UI 框架
│   ├── utils/         # 工具函数
│   └── ...            # 更多模块
├── plugins/           # 13 个官方插件
│   ├── agent-sdk-dev/
│   ├── claude-opus-4-5-migration/
│   ├── code-review/
│   ├── commit-commands/
│   ├── explanatory-output-style/
│   ├── feature-dev/
│   ├── frontend-design/
│   ├── hookify/
│   ├── learning-output-style/
│   ├── plugin-dev/
│   ├── pr-review-toolkit/
│   ├── ralph-wiggum/
│   └── security-guidance/
├── docs/              # 文档
├── README.md          # 本文件
├── ACKNOWLEDGEMENTS.md # 感谢声明
└── LICENSE            # 许可证说明
```

---

## 🚀 快速开始

### 运行 CLI

```bash
# 直接运行编译后的 CLI
node package/cli.js --version

# 查看帮助
node package/cli.js --help
```

### 学习源码

源码位于 `src/` 目录，包含 1,884 个 TypeScript/TSX 文件：

```bash
# 查看入口点
cat src/main.tsx

# 查看工具实现
ls src/tools/

# 查看命令实现
ls src/commands/
```

### 使用插件

插件位于 `plugins/` 目录，包含 13 个官方插件：

```bash
# 查看插件列表
ls plugins/

# 查看插件详情
cat plugins/ralph-wiggum/.claude-plugin/plugin.json
```

---

## 📊 项目统计

| 类别 | 数量 |
|------|------|
| TypeScript 源码 | 1,884 文件 |
| 工具实现 | 30+ 个 |
| 命令实现 | 50+ 个 |
| 服务模块 | 15+ 个 |
| UI 组件 | 25+ 个 |
| 官方插件 | 13 个 |
| 原生模块 | 2 个 (audio-capture, ripgrep) |

---

## 📜 许可证

本项目源码版权归 **Anthropic PBC** 所有。

本仓库仅供学习和研究使用，不代表 Anthropic 官方立场。

详见 [LICENSE](LICENSE) 和 [ACKNOWLEDGEMENTS.md](ACKNOWLEDGEMENTS.md)。

---

## 🔗 相关链接

- [Anthropic 官网](https://www.anthropic.com/)
- [Claude Code 文档](https://code.claude.com/)
- [本项目 GitHub](https://github.com/LING71671/Open-ClaudeCode)

---

*最后更新: 2026-03-31*
