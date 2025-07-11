# SuperClaude Commands Reference v2.0.1

## Table of Contents
- [Quick Start](#quick-start)
- [Universal Flags (Available on ALL Commands)](#universal-flags-available-on-all-commands)
- [Personas as Flags](#personas-as-flags)
- [Complete Command Reference](#complete-command-reference)
- [Flag Combinations & Best Practices](#flag-combinations--best-practices)

---

## Quick Start

**Basic Usage**: `/command [flags] [arguments]`

**Example Commands**:
```bash
/review --files src/ --quality --evidence    # Comprehensive code review with evidence
/analyze --code --persona-architect          # Code analysis with architect mindset
/build --react --magic --tdd                # Build React app with AI components
/troubleshoot --prod --five-whys --seq      # Production debugging with reasoning
/task:create "Add user authentication"       # Create and manage complex features
/deploy --env prod --plan --validate        # Safe production deployment
```

---

## Universal Flags (Available on ALL Commands)

### 🧠 Thinking Depth Control
| Flag | Description | Token Usage |
|------|-------------|-------------|
| `--think` | Multi-file analysis with expanded context | ~4K tokens |
| `--think-hard` | Architecture-level depth analysis | ~10K tokens |
| `--ultrathink` | Critical system analysis with maximum depth | ~32K tokens |

### 📦 Token Optimization
| Flag | Alias | Description |
|------|-------|-------------|
| `--uc` | `--ultracompressed` | Activate UltraCompressed mode (huge token reduction) |

### 🔧 MCP Server Control
| Flag | Description |
|------|-------------|
| `--c7` | Enable Context7 documentation lookup |
| `--seq` | Enable Sequential thinking analysis |
| `--magic` | Enable Magic UI component generation |
| `--pup` | Enable Puppeteer browser automation |
| `--all-mcp` | Enable all MCP servers for maximum capability |
| `--no-mcp` | Disable all MCP servers (native tools only) |
| `--no-c7` | Disable Context7 specifically |
| `--no-seq` | Disable Sequential thinking specifically |
| `--no-magic` | Disable Magic UI builder specifically |
| `--no-pup` | Disable Puppeteer specifically |

### 🔍 Analysis & Introspection
| Flag | Description |
|------|-------------|
| `--introspect` | Enable self-aware analysis with cognitive transparency |

### 📋 Planning & Execution
| Flag | Description |
|------|-------------|
| `--plan` | Show detailed execution plan before running |
| `--dry-run` | Preview changes without execution |
| `--watch` | Continuous monitoring with real-time feedback |
| `--interactive` | Step-by-step guided process |
| `--force` | Override safety checks (use with caution) |

### ✅ Quality & Validation
| Flag | Description |
|------|-------------|
| `--validate` | Enhanced pre-execution safety checks |
| `--security` | Security-focused analysis and validation |
| `--coverage` | Generate comprehensive coverage analysis |
| `--strict` | Zero-tolerance mode with enhanced validation |

---

## Personas as Flags

All personas are now integrated as flags, available on every command:

| Persona Flag | Expertise | Best For |
|--------------|-----------|----------|
| `--persona-architect` | Systems thinking, scalability, patterns | Architecture decisions, system design |
| `--persona-frontend` | UI/UX obsessed, accessibility-first | User interfaces, component design |
| `--persona-backend` | APIs, databases, reliability | Server architecture, data modeling |
| `--persona-analyzer` | Root cause analysis, evidence-based | Complex debugging, investigations |
| `--persona-security` | Threat modeling, zero-trust, OWASP | Security audits, vulnerability assessment |
| `--persona-mentor` | Teaching, guided learning, clarity | Documentation, knowledge transfer |
| `--persona-refactorer` | Code quality, maintainability | Code cleanup, technical debt |
| `--persona-performance` | Optimization, profiling, efficiency | Performance tuning, bottlenecks |
| `--persona-qa` | Testing, edge cases, validation | Quality assurance, test coverage |

---

## Complete Command Reference

### 🛠️ Development Commands (3)

#### `/build` - Universal Project Builder
Build projects, features, and components using modern stack templates.

**Command-Specific Flags:**
- `--init` - Initialize new project with stack setup
- `--feature` - Implement feature using existing patterns
- `--tdd` - Test-driven development workflow
- `--react` - React with Vite, TypeScript, Router
- `--api` - Express.js API with TypeScript
- `--fullstack` - Complete React + Node.js + Docker
- `--mobile` - React Native with Expo
- `--cli` - Commander.js CLI with testing

**Examples:**
```bash
/build --init --react --magic --tdd         # New React app with AI components
/build --feature "auth system" --tdd        # Feature with tests
/build --api --openapi --seq                # API with documentation
```

#### `/dev-setup` - Development Environment
Configure professional development environments with CI/CD and monitoring.

**Command-Specific Flags:**
- `--install` - Install and configure dependencies
- `--ci` - CI/CD pipeline configuration
- `--monitor` - Monitoring and observability setup
- `--docker` - Containerization setup
- `--testing` - Testing infrastructure
- `--team` - Team collaboration tools
- `--standards` - Code quality standards

**Examples:**
```bash
/dev-setup --install --ci --monitor         # Complete environment
/dev-setup --team --standards --docs        # Team setup
```

#### `/test` - Comprehensive Testing Framework
Create, run, and maintain testing strategies across the stack.

**Command-Specific Flags:**
- `--e2e` - End-to-end testing
- `--integration` - Integration testing
- `--unit` - Unit testing
- `--visual` - Visual regression testing
- `--mutation` - Mutation testing
- `--performance` - Performance testing
- `--accessibility` - Accessibility testing
- `--parallel` - Parallel test execution

**Examples:**
```bash
/test --coverage --e2e --pup               # Full test suite
/test --mutation --strict                  # Test quality validation
```

### 🔍 Analysis & Improvement Commands (5)

#### `/review` - AI-Powered Code Review
Comprehensive code review and quality analysis with evidence-based recommendations.

**Command-Specific Flags:**
- `--files` - Review specific files or directories
- `--commit` - Review changes in specified commit (HEAD, hash, range)
- `--pr` - Review pull request changes (git diff main..branch)
- `--quality` - Focus on code quality issues (DRY, SOLID, complexity)
- `--evidence` - Include sources and documentation for all suggestions
- `--fix` - Suggest specific fixes for identified issues
- `--summary` - Generate executive summary of review findings

**Examples:**
```bash
/review --files src/auth.ts --persona-security    # Security-focused file review
/review --commit HEAD --quality --evidence        # Quality review with sources
/review --pr 123 --all --interactive             # Comprehensive PR review
/review --files src/ --persona-performance --think # Performance analysis
```

#### `/analyze` - Multi-Dimensional Analysis
Comprehensive analysis of code, architecture, performance, and security.

**Command-Specific Flags:**
- `--code` - Code quality analysis
- `--architecture` - System design assessment
- `--profile` - Performance profiling
- `--deps` - Dependency analysis
- `--surface` - Quick overview
- `--deep` - Comprehensive analysis
- `--forensic` - Detailed investigation

**Examples:**
```bash
/analyze --code --architecture --seq       # Full analysis
/analyze --profile --deep --persona-performance  # Performance deep-dive
```

#### `/troubleshoot` - Professional Debugging
Systematic debugging and issue resolution.

**Command-Specific Flags:**
- `--investigate` - Systematic issue analysis
- `--five-whys` - Root cause analysis
- `--prod` - Production debugging
- `--perf` - Performance investigation
- `--fix` - Complete resolution
- `--hotfix` - Emergency fixes
- `--rollback` - Safe rollback

**Examples:**
```bash
/troubleshoot --prod --five-whys --seq    # Production RCA
/troubleshoot --perf --fix --pup          # Performance fix
```

#### `/improve` - Enhancement & Optimization
Evidence-based improvements with measurable outcomes.

**Command-Specific Flags:**
- `--quality` - Code structure improvements
- `--performance` - Performance optimization
- `--accessibility` - Accessibility improvements
- `--iterate` - Iterative improvement
- `--threshold` - Quality target percentage
- `--refactor` - Systematic refactoring
- `--modernize` - Technology updates

**Examples:**
```bash
/improve --quality --iterate --threshold 95%    # Quality improvement
/improve --performance --cache --pup            # Performance boost
```

#### `/explain` - Technical Documentation
Generate comprehensive explanations and documentation.

**Command-Specific Flags:**
- `--depth` - Complexity level (ELI5|beginner|intermediate|expert)
- `--visual` - Include diagrams
- `--examples` - Code examples
- `--api` - API documentation
- `--architecture` - System documentation
- `--tutorial` - Learning tutorials
- `--reference` - Reference docs

**Examples:**
```bash
/explain --depth expert --visual --seq     # Expert documentation
/explain --api --examples --c7             # API docs with examples
```

### ⚙️ Operations Commands (6)

#### `/deploy` - Application Deployment
Safe deployment with rollback capabilities.

**Command-Specific Flags:**
- `--env` - Target environment (dev|staging|prod)
- `--canary` - Canary deployment
- `--blue-green` - Blue-green deployment
- `--rolling` - Rolling deployment
- `--checkpoint` - Create checkpoint
- `--rollback` - Rollback to previous
- `--monitor` - Post-deployment monitoring

**Examples:**
```bash
/deploy --env prod --canary --monitor      # Canary production deploy
/deploy --rollback --env prod              # Emergency rollback
```

#### `/migrate` - Database & Code Migration
Safe migrations with rollback capabilities.

**Command-Specific Flags:**
- `--database` - Database migrations
- `--code` - Code migrations
- `--config` - Configuration migrations
- `--dependencies` - Dependency updates
- `--backup` - Create backup first
- `--rollback` - Rollback migration
- `--validate` - Data integrity checks

**Examples:**
```bash
/migrate --database --backup --validate    # Safe DB migration
/migrate --code --dry-run                  # Preview code changes
```

#### `/scan` - Security & Validation
Comprehensive security auditing and compliance.

**Command-Specific Flags:**
- `--owasp` - OWASP Top 10 compliance
- `--secrets` - Secret detection
- `--compliance` - Regulatory compliance
- `--quality` - Code quality validation
- `--automated` - Continuous monitoring

**Examples:**
```bash
/scan --security --owasp --deps           # Security audit
/scan --compliance --gdpr --strict        # Compliance check
```

#### `/estimate` - Project Estimation
Professional estimation with risk assessment.

**Command-Specific Flags:**
- `--detailed` - Comprehensive breakdown
- `--rough` - Quick estimation
- `--worst-case` - Pessimistic estimate
- `--agile` - Story point estimation
- `--complexity` - Technical assessment
- `--resources` - Resource planning
- `--timeline` - Timeline planning
- `--risk` - Risk assessment

**Examples:**
```bash
/estimate --detailed --complexity --risk   # Full estimation
/estimate --agile --story-points          # Agile planning
```

#### `/cleanup` - Project Maintenance
Professional cleanup with safety validations.

**Command-Specific Flags:**
- `--code` - Remove dead code
- `--files` - Clean build artifacts
- `--deps` - Remove unused dependencies
- `--git` - Clean git repository
- `--all` - Comprehensive cleanup
- `--aggressive` - Deep cleanup
- `--conservative` - Safe cleanup

**Examples:**
```bash
/cleanup --all --dry-run                  # Preview cleanup
/cleanup --code --deps --validate         # Code cleanup
```

#### `/git` - Git Workflow Management
Professional Git operations with safety features.

**Command-Specific Flags:**
- `--status` - Repository status
- `--commit` - Professional commit
- `--branch` - Branch management
- `--sync` - Remote synchronization
- `--checkpoint` - Create checkpoint
- `--merge` - Smart merge
- `--history` - History analysis
- `--pre-commit` - Setup and run pre-commit hooks

**Examples:**
```bash
/git --checkpoint "before refactor"       # Safety checkpoint
/git --commit --validate --test          # Safe commit
/git --pre-commit                        # Setup pre-commit hooks
/git --commit --pre-commit               # Commit with validation
```

### 🎨 Design & Architecture Commands (1)

#### `/design` - System Architecture
Professional system design with specifications.

**Command-Specific Flags:**
- `--api` - REST/GraphQL design
- `--ddd` - Domain-driven design
- `--microservices` - Microservices architecture
- `--event-driven` - Event patterns
- `--openapi` - OpenAPI specs
- `--graphql` - GraphQL schema
- `--bounded-context` - DDD contexts
- `--integration` - Integration patterns

**Examples:**
```bash
/design --api --ddd --openapi --seq      # API with DDD
/design --microservices --event-driven   # Microservices design
```

### 🔄 Workflow Commands (6)

#### `/cnb-cr` - CNB代码评审工作流
专门针对CNB平台的端到端代码评审自动化流程。

**⚠️ MCP依赖要求**：
- **CNB MCP服务器** - 必需，用于CNB平台API交互
- **WeChat Work MCP服务器** - 必需，用于团队通知

**Command-Specific Flags:**
- `--persona-qa` - QA专家视角评审
- `--persona-security` - 安全专家视角评审
- `--persona-performance` - 性能专家视角评审
- `--persona-frontend` - 前端专家视角评审
- `--persona-backend` - 后端专家视角评审
- `--dry-run` - 预览模式，不提交评论
- `--no-wecom` - 不发送WeChat Work通知
- `--force-clone` - 强制重新克隆仓库
- `--interactive` - 交互式确认每个步骤

**Key Features:**
- **智能PR解析**: 自动解析CNB PR链接获取详细信息
- **本地仓库管理**: 自动克隆/更新到 `~/Coding/cnb-cr/repos`
- **多维度分析**: 逻辑、风格、性能、安全、测试覆盖
- **结构化报告**: 生成专业的CR报告格式
- **自动化流程**: 一键完成评审、评论、通知全流程

**Examples:**
```bash
/cnb-cr https://cnb.tmeoa.com/kuwoFE/gundam/gdv1/-/pulls/57           # 基础代码评审
/cnb-cr [PR_URL] --persona-security --think-hard --strict             # 安全专家深度评审
/cnb-cr [PR_URL] --dry-run --interactive                              # 预览交互模式
```

#### `/gemini` - AI协作工作流
与Gemini CLI进行智能多轮协作的专业工作流程。

**核心功能:**
- **智能协作触发**: 自动识别协作需求，支持"请和Gemini商量着办"等自然触发
- **多轮对话管理**: 结构化的协作循环，保持上下文连贯性
- **响应整合分析**: 智能对比Claude和Gemini观点，提供综合建议
- **格式化输出**: 清晰的协作格式，突出双方观点和一致性分析

**Command-Specific Flags:**
- `--rounds <数量>` - 指定协作轮次限制
- `--max-output-tokens <数量>` - 控制Gemini响应长度
- `--auto-continue` - 自动继续协作模式
- `--format structured` - 结构化输出格式
- `--summary-only` - 仅显示关键摘要
- `--compress` - 压缩长响应内容
- `--validate` - 验证响应内容质量

**Key Features:**
- **智能触发**: 支持正则匹配和自然语言触发协作模式
- **PROMPT优化**: 自动构建包含上下文的高质量提示词
- **循环控制**: 智能的协作继续/停止判断机制
- **内容整合**: 双AI观点对比分析和互补建议生成
- **安全过滤**: 敏感信息检测和有害内容过滤

**Examples:**
```bash
/gemini 如何优化React组件性能？                    # 基础协作咨询
/gemini --think-hard --rounds 3 微服务架构设计      # 深度协作分析
/gemini --format structured --validate API设计方案  # 结构化协作评估
```

#### `/spawn` - Specialized Agents
Spawn focused agents for parallel tasks.

**Command-Specific Flags:**
- `--task` - Define specific task
- `--parallel` - Concurrent execution
- `--specialized` - Domain expertise
- `--collaborative` - Multi-agent work
- `--sync` - Synchronize results
- `--merge` - Merge outputs

**Examples:**
```bash
/spawn --task "frontend tests" --parallel  # Parallel testing
/spawn --collaborative --sync              # Team simulation
```

#### `/document` - Documentation Creation
Professional documentation in multiple formats.

**Command-Specific Flags:**
- `--user` - User guides
- `--technical` - Developer docs
- `--markdown` - Markdown format
- `--interactive` - Interactive docs
- `--multilingual` - Multi-language
- `--maintain` - Maintenance plan

**Examples:**
```bash
/document --api --interactive --examples   # API documentation
/document --user --visual --multilingual   # User guides
```

#### `/load` - Project Context Loading
Load and analyze project context.

**Command-Specific Flags:**
- `--depth` - Analysis depth (shallow|normal|deep)
- `--context` - Context preservation
- `--patterns` - Pattern recognition
- `--relationships` - Dependency mapping
- `--structure` - Project structure
- `--health` - Project health
- `--standards` - Coding standards

**Examples:**
```bash
/load --depth deep --patterns --seq       # Deep analysis
/load --structure --health --standards   # Project assessment
```

#### `/task` - Task Management
Complex feature management across sessions with automatic breakdown and recovery.

**Command-Specific Operations:**
- `/task:create [description]` - Create new task with automatic breakdown
- `/task:status [task-id]` - Check task status and progress
- `/task:resume [task-id]` - Resume work after break
- `/task:update [task-id] [updates]` - Update task progress and requirements
- `/task:complete [task-id]` - Mark task as done with summary

**Key Features:**
- **Smart Breakdown**: Automatic complexity analysis and subtask creation
- **Context Preservation**: Save working state across sessions
- **Progress Tracking**: Automatic updates and blocker detection
- **Session Recovery**: Resume from checkpoints with full context

**Examples:**
```bash
/task:create "Implement OAuth 2.0 authentication system"  # Create complex feature
/task:status oauth-task-id                               # Check progress
/task:resume oauth-task-id                               # Resume after break
/task:update oauth-task-id "Found library conflict"      # Update with discoveries
/task:complete oauth-task-id                             # Complete with summary
```

---

## Flag Combinations & Best Practices

### 🚀 Professional Workflows

**Full-Stack Development**
```bash
/design --api --ddd --persona-architect
/build --fullstack --tdd --magic
/test --coverage --e2e --pup
/deploy --env staging --validate
```

**Security-First Development**
```bash
/scan --security --owasp --deps --persona-security
/analyze --security --forensic --seq
/improve --security --validate --strict
/test --security --coverage
```

**Performance Optimization**
```bash
/analyze --profile --deep --persona-performance
/troubleshoot --perf --investigate --pup
/improve --performance --iterate --threshold 90%
/test --performance --load
```

**Quality Assurance**
```bash
/review --quality --evidence --persona-qa
/improve --quality --refactor --strict
/scan --validate --quality
/test --coverage --mutation
```

### 💡 Best Practices

1. **Always validate risky operations**
   ```bash
   /deploy --env prod --validate --plan
   /migrate --database --dry-run --backup
   ```

2. **Use personas for specialized expertise**
   ```bash
   /analyze --architecture --persona-architect
   /scan --security --persona-security
   ```

3. **Combine MCP servers for maximum capability**
   ```bash
   /build --react --magic --seq --c7
   /test --e2e --pup --coverage
   ```

4. **Progressive thinking for complex tasks**
   ```bash
   /troubleshoot --investigate --think
   /design --microservices --think-hard
   /analyze --architecture --ultrathink
   ```

### 🎯 Quick Reference

**High-Risk Operations**: Always use `--validate` or `--dry-run`
**Documentation Tasks**: Enable `--c7` for library lookups
**Complex Analysis**: Use `--seq` for reasoning
**UI Development**: Enable `--magic` for AI components
**Testing**: Use `--pup` for browser automation
**Token Saving**: Add `--uc` for 70% reduction

---

**SuperClaude v2.0.1** - 19 professional commands | 9 cognitive personas | Advanced MCP integration | Evidence-based methodology
