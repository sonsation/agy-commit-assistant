# 🤖 Gemini Commit Assistant

![screenshot](./screenshot.gif)

**English** | [한국어](README.ko.md)

AI-powered commit message generator using Google Gemini CLI (Gemini 2.5 Flash) with **Korean/English language support**.

## 📦 Installation

```bash
npm install -g gemini-commit-assistant
```

## 🚀 Usage

```bash
# Generate commit message for staged files
git add file1.js file2.js
aic # or ai-commit

# Stage all files and generate commit message
aic --all # ai-commit --all

# Configure language (Korean/English)
aic --configure # ai-commit --configure

# Set up git alias (optional)
aic --setup # ai-commit --setup
git aic  # git ai-commit
```

## 🔧 Options

| Option         | Description                                      |
| -------------- | ------------------------------------------------ |
| `--all`, `-a`  | Stage all files before generating commit message |
| `--configure`  | Change language / AI CLI / model settings        |
| `--provider`   | Use a specific AI CLI for this run (`agy` \| `claude`) |
| `--setup`      | Set up git alias (`git aic`)                     |
| `--unsetup`    | Remove git alias                                 |
| `--help`, `-h` | Show help                                        |

## 🤖 Choosing an AI CLI (agy / claude)

You can pick which AI CLI generates your commit messages.

- **`agy`** — Antigravity CLI (Gemini) · default
- **`claude`** — Claude Code CLI

```bash
aic --configure         # interactively pick AI CLI + model (global/local)
aic --provider claude   # use claude for this run only
aic --claude            # shorthand for the above
aic --agy               # use agy for this run only
```

The choice is stored as `"provider"` in both the global config
(`~/.gemini-commit-config.json`) and the per-project `.aicrc`, with the
project config taking precedence.

## 💰 Cost Benefits

**Gemini CLI Personal Account (Recommended):**

- **60 requests/minute + 1,000 requests/day** - FREE
- 10x higher limits than API key approach
- Sustainable for entire teams

**API Key Approach:**

- Only 100 requests/day - LIMITED

## 📋 Requirements

- Node.js 16.0.0+
- Git 2.0+
- **Gemini CLI** (install: `npm install -g @google/gemini-cli`)
- **Google account** (personal account recommended)

## 🌐 Language Support

First run automatically prompts for language selection (Korean/English).
Change anytime with `aic --configure`.

## 🛠️ Setup

```bash
# Install Gemini CLI
npm install -g @google/gemini-cli

gemini # Authenticate with Google Account
```

## 🎯 Examples

**Korean Mode:**

```bash
aic
# 🤖 AI 커밋 메시지 생성기 (Gemini 기반)
# "feat: 사용자 인증 시스템 구현"
```

**English Mode:**

```bash
aic
# 🤖 AI Commit CLI - AI-powered commit message generator
# "feat: Implement user authentication system"
```

## 📄 License

MIT License
