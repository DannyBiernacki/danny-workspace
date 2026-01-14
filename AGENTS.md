# Agent Skills

This project has skills available in `.claude/skills/`. The AI agent can dynamically load these skills when needed.

## Available Skills

<available_skills>
  <skill name="dev-browser" category="automation" path=".claude/skills/automation/dev-browser">
    Browser automation with persistent page state. Use when users ask to navigate websites, fill forms, take screenshots, extract web data, test web apps, or automate browser workflows.
  </skill>
  
  <skill name="gastown" category="tools" path=".claude/skills/tools/gastown">
    Multi-agent orchestrator for Claude Code. Use when user mentions gastown, gas town, gt commands, convoys, polecats, rigs, slinging work, multi-agent coordination, beads, hooks, the witness, the mayor, the refinery, or wants to run multiple AI agents on projects simultaneously.
  </skill>
  
  <skill name="zai-cli" category="tools" path=".claude/skills/tools/zai-cli">
    Z.AI CLI providing: Vision (image/video analysis, OCR, UI-to-code, error diagnosis with GLM-4.6V), Search (real-time web search with domain/recency filtering), Reader (web page to markdown extraction), Repo (GitHub code search and reading via ZRead), Tools (MCP tool discovery and raw calls), Code (TypeScript tool chaining). Use for visual content analysis, web search, page reading, or GitHub exploration. Requires Z_AI_API_KEY.
  </skill>
  
  <skill name="orchestration" category="workflow" path=".claude/skills/workflow/orchestration">
    Multi-agent orchestration for complex tasks using cc-mirror tasks and TodoWrite. Use when tasks require parallel work, multiple agents, sophisticated coordination, or decomposition into parallel subtasks.
  </skill>
</available_skills>

## How Skills Work

Skills use a "progressive disclosure" mechanism:

1. The agent scans this file to see available skills
2. When a skill is relevant, the agent loads the full `SKILL.md`
3. The agent follows the instructions in `SKILL.md` to complete the task

## Installing More Skills

```bash
# Universal installer
openskills install numman-ali/n-skills

# Sync to update AGENTS.md
openskills sync
```

## Skill Sources

- **dev-browser**: Synced from SawyerHood/dev-browser
- **gastown**: Native n-skills skill
- **zai-cli**: Native n-skills skill  
- **orchestration**: Native n-skills skill

All skills from: <https://github.com/numman-ali/n-skills>
