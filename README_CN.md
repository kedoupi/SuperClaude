# SuperClaude – Claude Code 开发框架

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-2.0.1-blue.svg)](https://github.com/NomenAK/SuperClaude)
[![GitHub issues](https://img.shields.io/github/issues/NomenAK/SuperClaude)](https://github.com/NomenAK/SuperClaude/issues)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/NomenAK/SuperClaude/blob/master/CONTRIBUTING.md)

**一个为 Claude Code 提供专业化命令、认知人格和开发方法论的配置框架。**

[English](README.md) | 中文

## 🚀 2.0.1 版本更新

**重要提示：** 请先删除 .claude 目录中的旧文件（RULES.md、MCP.md、PERSONAS.md、CLAUDE.md 和 /commands 目录）以全新开始

SuperClaude v2 引入了专注于可维护性和可扩展性的架构改进：

- **⚡ 精简架构**：采用 @include 引用系统进行配置管理
- **🎭 人格标志化**：9 个认知人格集成到标志系统（`--persona-architect`、`--persona-security` 等）
- **📦 增强安装器**：install.sh 支持更新模式、试运行、备份处理和平台检测
- **🔧 模块化设计**：用于添加新命令和功能的模板系统
- **🎯 统一体验**：所有命令间一致的标志行为

查看 [ROADMAP.md](ROADMAP.md) 了解未来开发想法和贡献机会。

## 🎯 背景

Claude Code 提供强大的功能，但在以下方面可进一步增强：
- **不同技术领域的专业知识**
- **复杂项目的令牌效率**  
- **基于证据的开发方法**
- **调试会话期间的上下文保持**
- **各种任务的领域特定思维**

## ✨ SuperClaude 特性

SuperClaude 为 Claude Code 增强了：
- **19 个专业化命令** 覆盖开发生命周期任务
- **9 个认知人格** 提供领域特定方法
- **令牌优化** 支持压缩选项
- **基于证据的方法论** 鼓励文档化
- **MCP 集成** 支持 Context7、Sequential、Magic、Puppeteer
- **Git 检查点支持** 安全实验
- **内省模式** 用于框架改进和故障排除

## 🚀 安装

### 增强安装器 v2.0.1
安装器提供多种选项：

```bash
git clone https://github.com/NomenAK/SuperClaude.git
cd SuperClaude

# 基础安装
./install.sh                           # 默认：~/.claude/

# 高级选项
./install.sh --dir /opt/claude        # 自定义位置
./install.sh --update                 # 更新现有安装
./install.sh --dry-run --verbose      # 详细预览变更
./install.sh --force                  # 跳过确认（自动化）
./install.sh --log install.log        # 记录所有操作
```

**v2.0.1 安装器特性：**
- 🔄 **更新模式**：在更新时保留自定义设置
- 👁️ **试运行**：应用前预览变更
- 💾 **智能备份**：带时间戳的自动备份
- 🧹 **清理更新**：移除过时文件
- 🖥️ **平台检测**：支持 Linux、macOS、WSL
- 📊 **进度跟踪**：安装反馈

零依赖，默认安装到 `~/.claude/`。

**注意：** 安装后，所有配置文件位于 `~/.claude/`（您的主目录），而非项目目录。

## 💡 核心能力

### 🧠 **认知人格（现已标志化！）**
通过人格标志在不同方法间切换：

```bash
/analyze --code --persona-architect     # 系统思维方法
/build --react --persona-frontend       # 专注用户体验的开发  
/scan --security --persona-security     # 安全优先分析
/troubleshoot --prod --persona-analyzer # 根本原因分析方法
```

**v2.0.1 更新**：所有 9 个人格现在都是通用标志，在每个命令上都可用，以便一致地访问专业化方法。

### ⚡ **19 个命令**
开发生命周期覆盖：

**开发命令**
```bash
/build --react --magic --tdd    # 使用 AI 组件开发
/dev-setup --ci --monitor       # 环境设置
/test --coverage --e2e --pup    # 测试策略
```

**分析与质量**
```bash
/review --quality --evidence --persona-qa     # AI 驱动的代码审查
/analyze --architecture --seq   # 系统分析
/troubleshoot --prod --five-whys # 问题解决
/improve --performance --iterate # 优化
/explain --depth expert --visual # 文档化
```

**运营与安全**
```bash
/deploy --env prod --plan       # 部署规划
/scan --security --owasp --deps # 安全审计
/migrate --dry-run --rollback   # 数据库迁移
/cleanup --all --validate       # 维护任务
```

### 🎛️ **MCP 集成**
- **Context7**：访问库文档
- **Sequential**：多步推理能力
- **Magic**：AI 生成的 UI 组件
- **Puppeteer**：浏览器测试和自动化

**⚠️ 重要：** SuperClaude 不包含 MCP 服务器。您需要在 Claude Code 的 MCP 设置中单独安装它们才能使用 MCP 相关标志（--c7、--seq、--magic、--pup）。

### 📊 **令牌效率**
SuperClaude 的 @include 模板系统有助于管理令牌使用：
- **超压缩模式** 选项用于令牌减少
- **模板引用** 用于配置管理
- **缓存机制** 避免冗余
- **上下文感知压缩** 选项

## 🎮 示例工作流

### 企业架构流程
```bash
/design --api --ddd --bounded-context --persona-architect    # 领域驱动设计
/estimate --detailed --worst-case --seq                      # 资源规划
/scan --security --validate --persona-security               # 安全审查
/build --api --tdd --coverage --persona-backend              # 实现
```

### 生产问题解决
```bash
/troubleshoot --investigate --prod --persona-analyzer        # 分析
/analyze --profile --perf --seq                             # 性能审查
/improve --performance --threshold 95% --persona-performance # 优化
/test --integration --e2e --pup                             # 验证
```

### 框架故障排除与改进
```bash
/troubleshoot --introspect                                  # 调试 SuperClaude 行为
/analyze --introspect --seq                                 # 分析框架模式
/improve --introspect --uc                                  # 优化令牌使用
```

### 全栈功能开发
```bash
/build --react --magic --watch --persona-frontend           # UI 开发
/test --coverage --e2e --strict --persona-qa                # 质量保证
/scan --validate --deps --persona-security                  # 安全检查
```

## 🎭 可用人格

| 人格 | 专注领域 | 工具 | 用例 |
|---------|-----------|-------|-----------|
| **architect** | 系统设计 | Sequential, Context7 | 架构规划 |
| **frontend** | 用户体验 | Magic, Puppeteer, Context7 | UI 开发 |
| **backend** | 服务器系统 | Context7, Sequential | API 开发 |
| **security** | 安全分析 | Sequential, Context7 | 安全审查 |
| **analyzer** | 问题解决 | 所有 MCP 工具 | 调试 |
| **qa** | 质量保证 | Puppeteer, Context7 | 测试 |
| **performance** | 优化 | Puppeteer, Sequential | 性能调优 |
| **refactorer** | 代码质量 | Sequential, Context7 | 代码改进 |
| **mentor** | 知识分享 | Context7, Sequential | 文档化 |

## 🛠️ 配置选项

### 思考深度控制
```bash
# 标准分析
/analyze --think

# 深度分析  
/design --think-hard

# 最大深度
/troubleshoot --ultrathink
```

### 内省模式
```bash
# 为 SuperClaude 改进启用自我感知分析
/analyze --introspect

# 调试 SuperClaude 行为
/troubleshoot --introspect --seq

# 优化框架性能
/improve --introspect --persona-performance
```

### 令牌管理
```bash
# 标准模式
/build --react --magic

# 使用压缩
/analyze --architecture --uc

# 仅原生工具
/scan --security --no-mcp
```

### 基于证据的开发
SuperClaude 鼓励：
- 为设计决策编写文档
- 为质量改进进行测试
- 为性能工作提供指标
- 为部署进行安全验证
- 为架构选择进行分析

## 📋 命令分类

### 开发（3 个命令）
- `/build` - 带技术栈模板的项目构建器
- `/dev-setup` - 开发环境设置
- `/test` - 测试框架

### 分析与改进（5 个命令）
- `/review` - AI 驱动的代码审查，提供基于证据的建议
- `/analyze` - 代码和系统分析
- `/troubleshoot` - 调试和问题解决
- `/improve` - 增强和优化
- `/explain` - 文档化和说明

### 运营（6 个命令）
- `/deploy` - 应用部署
- `/migrate` - 数据库和代码迁移
- `/scan` - 安全和验证
- `/estimate` - 项目估算
- `/cleanup` - 项目维护
- `/git` - Git 工作流管理

### 设计与工作流（5 个命令）
- `/design` - 系统架构
- `/spawn` - 并行任务执行
- `/document` - 文档创建
- `/load` - 项目上下文加载
- `/task` - 任务管理

## 🔧 技术架构 v2

SuperClaude v2 的架构支持可扩展性：

**🏗️ 模块化配置**
- **CLAUDE.md** – 带 @include 引用的核心配置
- **.claude/shared/** – 集中式 YAML 模板
- **commands/shared/** – 可重用命令模式
- **@include 系统** – 配置模板引擎

**🎯 统一命令系统**
- **19 个命令** – 开发生命周期覆盖
- **标志继承** – 所有命令的通用标志
- **人格集成** – 9 个认知模式作为标志
- **模板验证** – 引用完整性检查

**📦 架构优势**
- **单一真实来源** – 集中式更新
- **易于扩展** – 添加新命令/标志
- **一致行为** – 统一标志处理
- **减少重复** – 基于模板的配置

**✅ 质量特性**
- **基于证据的方法** – 鼓励文档化
- **研究集成** – 库文档访问
- **错误恢复** – 优雅的失败处理
- **结构化输出** – 有组织的文件位置

## 📊 对比

| 方面 | 标准 Claude Code | SuperClaude 框架 |
|--------|---------------------|----------------------|
| **专业知识** | 通用响应 | 9 个专业化人格 |
| **命令** | 手动指令 | 19 个工作流命令 |
| **上下文** | 基于会话 | Git 检查点支持 |
| **令牌** | 标准使用 | 压缩选项 |
| **方法** | 通用目的 | 基于证据 |
| **文档** | 按需 | 系统化方法 |
| **质量** | 可变 | 验证模式 |
| **集成** | 基础工具 | MCP 编排 |

## 🔮 用例

**开发团队**
- 跨领域的一致方法
- 标准化工作流
- 基于证据的决策
- 文档实践

**技术负责人**
- 架构审查
- 性能优化
- 代码质量改进
- 团队知识分享

**运营**
- 部署程序
- 调试工作流
- 安全管理
- 维护任务

## 🎯 适用性

**适合于：**
- ✅ 希望获得一致 AI 辅助的团队
- ✅ 需要专业化方法的项目
- ✅ 基于证据的开发实践
- ✅ 令牌敏感的工作流
- ✅ 领域特定专业知识需求

**可能不适合：**
- ❌ 纯手动工作流
- ❌ 最小配置偏好
- ❌ 临时开发风格
- ❌ 单一领域专注

## 🚦 开始使用

1. **安装 SuperClaude**
   ```bash
   git clone https://github.com/NomenAK/SuperClaude.git && cd SuperClaude && ./install.sh
   ```

2. **验证安装**
   ```bash
   /load                                    # 加载项目上下文
   /analyze --code --think                  # 测试分析
   /analyze --architecture --persona-architect  # 尝试人格
   ```

3. **示例工作流**
   ```bash
   /design --api --ddd            # 架构设计
   /build --feature --tdd         # 实现
   /test --coverage --e2e         # 质量保证
   /deploy --env staging --plan   # 部署
   ```

## 🛟 支持

- **安装帮助**：运行 `./install.sh --help`
- **命令详情**：查看 `~/.claude/commands/`
- **贡献**：查看 [CONTRIBUTING.md](CONTRIBUTING.md)
- **问题**：[GitHub Issues](https://github.com/NomenAK/SuperClaude/issues)

## 🤝 社区

SuperClaude 欢迎贡献：
- **新人格** 用于专业化工作流
- **命令** 用于领域特定操作  
- **模式** 用于开发实践
- **集成** 用于生产力工具

加入社区：[讨论区](https://github.com/NomenAK/SuperClaude/discussions)

## 📈 版本 2.0.1 变更

**🎯 架构改进：**
- **配置管理**：@include 引用系统
- **令牌效率**：保持压缩选项
- **命令系统**：统一标志继承
- **人格系统**：现在作为标志可用
- **安装器**：使用新模式增强
- **维护**：集中式配置

**📊 框架详情：**
- **命令**：19 个专业化命令
- **人格**：9 个认知方法
- **MCP 服务器**：4 个集成
- **方法论**：基于证据的方法
- **使用者**：开发团队

## 🎉 增强您的开发

SuperClaude 为使用 Claude Code 提供了结构化方法，包含专业化命令、人格和开发模式。

---

*SuperClaude v2.0.1 – Claude Code 开发框架*

[⭐ GitHub 星标](https://github.com/NomenAK/SuperClaude) | [💬 讨论](https://github.com/NomenAK/SuperClaude/discussions) | [🐛 报告问题](https://github.com/NomenAK/SuperClaude/issues)