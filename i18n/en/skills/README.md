# 🎯 AI Skills Library

The `i18n/zh/skills/` directory stores AI Skills. These are advanced capability encapsulations, more sophisticated than simple prompts, that enable AI to perform at an expert level in specific domains. Currently includes **14** professional skills.

## Directory Structure

```
i18n/zh/skills/
├── README.md                # This file
│
├── # === Meta Skills (Core) ===
├── claude-skills/           # ⭐ Meta Skill: Skills for Generating Skills (11KB)
│
├── # === Claude Tools ===
├── claude-code-guide/       # Guide for using Claude Code (9KB)
├── claude-cookbooks/        # Best practices for Claude API (9KB)
│
├── # === Databases ===
├── postgresql/              # ⭐ PostgreSQL Expert Skill (76KB, most detailed)
├── timescaledb/             # Time-series Database Extension (3KB)
│
├── # === Cryptocurrency / Quant ===
├── ccxt/                    # Unified Cryptocurrency Exchange API (18KB)
├── coingecko/               # CoinGecko Market Data API (3KB)
├── cryptofeed/              # Cryptocurrency Real-time Data Stream (6KB)
├── hummingbot/              # Quant Trading Bot Framework (4KB)
├── polymarket/              # Prediction Market API (6KB)
│
├── # === Development Tools ===
├── telegram-dev/            # Telegram Bot Development (18KB)
├── twscrape/                # Twitter/X Data Scraping (11KB)
├── snapdom/                 # DOM Snapshot Tool (8KB)
└── proxychains/             # Proxy Chains Configuration (6KB)
```

## Skills Overview Table

### Sorted by File Size (Detail Level)

| Skill | Size | Domain | Description |
|---|---|---|---|
| **postgresql** | 76KB | Database | ⭐ Most detailed, complete PostgreSQL expert skill |
| **telegram-dev** | 18KB | Bot Development | Complete guide for Telegram Bot development |
| **ccxt** | 18KB | Trading | Unified API for cryptocurrency exchanges |
| **twscrape** | 11KB | Data Collection | Twitter/X data scraping |
| **claude-skills** | 11KB | Meta Skill | ⭐ Skills for Generating Skills |
| **claude-code-guide** | 9KB | Tools | Best practices for Claude Code usage |
| **claude-cookbooks** | 9KB | Tools | Claude API usage examples |
| **snapdom** | 8KB | Frontend | DOM snapshots and testing |
| **cryptofeed** | 6KB | Data Stream | Cryptocurrency real-time data stream |
| **polymarket** | 6KB | Prediction Market | Polymarket API integration |
| **proxychains** | 6KB | Network | Proxy chains configuration and usage |
| **hummingbot** | 4KB | Quant | Quant trading bot framework |
| **timescaledb** | 3KB | Database | PostgreSQL time-series extension |
| **coingecko** | 3KB | Market Data | CoinGecko Market Data API |

### Categorized by Domain

#### 🔧 Meta Skills & Tools

| Skill | Description | Recommended Scenarios |
|---|---|---|
| `claude-skills` | Skills for Generating Skills | Essential for creating new skills |
| `claude-code-guide` | Claude Code CLI Usage Guide | Daily development |
| `claude-cookbooks` | Claude API Best Practices | API integration |

#### 🗄️ Databases

| Skill | Description | Recommended Scenarios |
|---|---|---|
| `postgresql` | Complete PostgreSQL Guide (76KB) | Relational database development |
| `timescaledb` | Time-series Database Extension | Time-series data |

#### 💰 Cryptocurrency / Quant

| Skill | Description | Recommended Scenarios |
|---|---|---|
| `ccxt` | Unified Exchange API | Multi-exchange integration |
| `coingecko` | Market Data API | Price queries |
| `cryptofeed` | Real-time Data Stream | WebSocket market data |
| `hummingbot` | Quant Trading Framework | Automated trading |
| `polymarket` | Prediction Market API | Prediction market trading |

#### 🛠️ Development Tools

| Skill | Description | Recommended Scenarios |
|---|---|---|
| `telegram-dev` | Telegram Bot Development | Bot development |
| `twscrape` | Twitter Data Scraping | Social media data |
| `snapdom` | DOM Snapshots | Frontend testing |
| `proxychains` | Proxy Chains Configuration | Network proxy |

## Difference Between Skills vs Prompts

| Dimension | Prompts | Skills |
|---|---|---|
| Granularity | Single task instruction | Complete capability encapsulation |
| Reusability | Copy-paste | Automatically effective after configuration |
| Context | Needs manual provision | Built-in domain knowledge |
| Use Case | Temporary tasks | Long-term projects |
| Structure | Single file | Directory (includes assets/scripts/references) |

## Skill Directory Structure

Each skill follows a unified structure:

```
skill-name/
├── SKILL.md         # Main skill file, contains domain knowledge and rules
├── assets/          # Static resources (images, config templates, etc.)
├── scripts/         # Helper scripts
└── references/      # Reference documents
```

## Quick Start

### 1. View a Skill

```bash
# View meta-skill
cat i18n/zh/skills/claude-skills/SKILL.md

# View PostgreSQL skill (most detailed)
cat i18n/zh/skills/postgresql/SKILL.md

# View Telegram Bot development skill
cat i18n/zh/skills/telegram-dev/SKILL.md
```

### 2. Copy to Project for Use

```bash
# Copy entire skill directory
cp -r i18n/zh/skills/postgresql/ ./my-project/

# Or just copy main file to CLAUDE.md
cp i18n/zh/skills/postgresql/SKILL.md ./CLAUDE.md
```

### 3. Use with Claude Code

Create `CLAUDE.md` in the project root, referencing skills:

```markdown
# Project Rules

Please refer to the following skill files:
@i18n/zh/skills/postgresql/SKILL.md
@i18n/zh/skills/telegram-dev/SKILL.md
```

## Create Custom Skill

### Method 1: Generate using Meta Skill (Recommended)

1. Prepare domain materials (documents, code, specifications)
2. Provide materials along with `i18n/zh/skills/claude-skills/SKILL.md` to AI
3. AI will generate a dedicated Skill for that domain

```bash
# Example: Let AI generate a new skill after reading the meta-skill
cat i18n/zh/skills/claude-skills/SKILL.md
# Then tell AI: Based on this meta-skill, please generate a new SKILL.md for [your domain]
```

### Method 2: Manual Creation

```bash
# Create skill directory
mkdir -p i18n/zh/skills/my-skill/{assets,scripts,references}

# Create main file
cat > i18n/zh/skills/my-skill/SKILL.md << 'EOF'
# My Skill

## Overview
Briefly describe skill purpose and applicable scenarios

## Domain Knowledge
- Core concepts
- Best practices
- Common patterns

## Rules & Constraints
- Mandatory rules
- Prohibited operations
- Boundary conditions

## Examples
Specific usage examples and code snippets

## FAQ
FAQ and solutions
EOF
```

## Core Skill Details

### `claude-skills/SKILL.md` - Meta Skill ⭐

**Skills for Generating Skills**, is the core tool for creating new skills.

Usage:
1. Prepare your domain materials (documents, code, specifications, etc.)
2. Provide materials along with SKILL.md to AI
3. AI will generate a dedicated Skill for that domain

### `postgresql/SKILL.md` - PostgreSQL Expert ⭐

The most detailed skill (76KB), includes:
- Database design best practices
- Query optimization techniques
- Indexing strategies
- Performance tuning
- Common problem solutions
- SQL code examples

### `telegram-dev/SKILL.md` - Telegram Bot Development

Complete Telegram Bot development guide (18KB):
- Bot API usage
- Message handling
- Keyboards and callbacks
- Webhook configuration
- Error handling

### `ccxt/SKILL.md` - Cryptocurrency Exchange API

Unified exchange API encapsulation (18KB):
- Supports 100+ exchanges
- Unified data format
- Order management
- Market data retrieval

## Related Resources

- [Skills Generator](https://github.com/yusufkaraaslan/Skill_Seekers) - Convert any material into AI Skills
- [Meta Skill File](./claude-skills/SKILL.md) - Skills for Generating Skills
- [Prompt Library](../prompts/) - More granular prompt collections
- [Claude Code Guide](./claude-code-guide/SKILL.md) - Claude Code Usage Best Practices
- [Document Library](../documents/) - Methodologies and development experiences