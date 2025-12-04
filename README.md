# 🎪 Feedback Triage System

Automated feedback triage system for the Winter Festival using GitHub Actions and goose.

## 🎯 Overview

This system automatically categorizes and triages feedback issues submitted to the festival, helping coordinators prioritize and respond to problems quickly.

## 🤖 How It Works

1. **Issue Creation**: When a new issue is created in this repository
2. **Automatic Triage**: GitHub Actions triggers a workflow that:
   - Analyzes the issue title and body
   - Categorizes it (URGENT, FEATURE_REQUEST, QUESTION)
   - Assigns priority (HIGH, MEDIUM, LOW)
   - Adds appropriate labels
   - Posts an automated response

## 📋 Categories

- **🚨 URGENT**: Critical issues requiring immediate attention (heating failures, safety concerns)
- **💡 FEATURE_REQUEST**: Suggestions for improvements or new features
- **❓ QUESTION**: Information requests or clarifications needed

## 🏷️ Labels

The system automatically applies labels:
- `urgent` - Critical issues
- `bug` - Something isn't working
- `enhancement` - New feature or request
- `feature-request` - Feature suggestions
- `question` - Questions needing answers
- `priority:high` / `priority:medium` / `priority:low` - Priority levels

## 🚀 Setup

### Prerequisites
- GitHub account
- GitHub CLI (`gh`) installed
- LLM API key (OpenAI, Anthropic, etc.)

### Configuration

1. **Add API Key as Secret**:
   ```bash
   gh secret set LLM_API_KEY
   ```
   Then paste your API key when prompted.

2. **Test the System**:
   Create a test issue to see the automation in action!

## 📝 Example Issues

See the initial issues created for the Winter Festival:
- Issue #1: Heating system emergency
- Issue #2: Photo booth feature request
- Issue #3: Lost and found location question

## 🛠️ Technical Details

- **Workflow File**: `.github/workflows/triage.yml`
- **Trigger**: On issue creation (`issues: [opened]`)
- **Runtime**: Ubuntu latest with Python 3.11
- **Tools**: GitHub CLI, Python, goose-ai

## 📊 Monitoring

Check the **Actions** tab to see:
- Workflow runs
- Triage results
- Any errors or issues

## 🤝 Contributing

To improve the triage logic:
1. Edit `.github/workflows/triage.yml`
2. Modify the categorization rules in the Python script
3. Test with sample issues
4. Submit a pull request

---

Built with ❤️ using goose and GitHub Actions
