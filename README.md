# .NET Agent Skills

[![Dashboard](https://github.com/dotnet/skills/actions/workflows/pages/pages-build-deployment/badge.svg)](https://dotnet.github.io/skills/)

This repository contains the .NET team's curated set of core skills and custom agents for coding agents. For information about the Agent Skills standard, see [agentskills.io](https://agentskills.io).

## What's Included

| Plugin | Description |
|--------|-------------|
| [release](plugins/release/) | Stable .NET agent skills for everyday development: coding, diagnostics, performance, MSBuild, testing, NuGet, templates, upgrades, data access, MAUI, and AI. |
| [experimental](plugins/experimental/) | Experimental .NET agent skills under active evaluation. These skills may change or be promoted to release. |

## Installation

### 🚀 Plugins - Copilot CLI / Claude Code

1. Launch Copilot CLI or Claude Code
2. Add the marketplace:
   ```
   /plugin marketplace add dotnet/skills
   ```
3. Install a plugin:
   ```
   /plugin install <plugin>@dotnet-agent-skills
   ```
4. Restart to load the new plugins
5. View available skills:
   ```
   /skills
   ```
6. View available agents:
   ```
   /agents
   ```
7. Update plugin (on demand):
   ```
   /plugin update <plugin>@dotnet-agent-skills
   ```

### VS Code / VS Code Insiders (Preview)

> [!IMPORTANT]  
> VS Code plugin support is a preview feature and subject to change. You may need to enable it first.

```jsonc
// settings.json
{
  "chat.plugins.enabled": true,
  "chat.plugins.marketplaces": ["dotnet/skills"]
}
```

Once configured, type `/plugins` in Copilot Chat or use the `@agentPlugins` filter in Extensions to browse and install plugins from the marketplace.

### Codex CLI

Skills in this repository follow the [agentskills.io](https://agentskills.io) open standard
and are compatible with [OpenAI Codex](https://developers.openai.com/codex/skills).

Install individual skills using the `skill-installer` CLI with the GitHub URL:

```bash
$ skill-installer install https://github.com/dotnet/skills/tree/main/plugins/<plugin>/skills/<skill-name>
```

### ⚡ Agentic Workflows

Some plugins include [GitHub Agentic Workflow](https://github.com/github/gh-aw) templates for CI/CD automation:

1. Install the `gh aw` CLI extension
2. Copy the desired workflow `.md` files and the `shared/` directory to your repository's `.github/workflows/`
3. Compile and commit:
   ```
   gh aw compile
   ```
4. Commit both the `.md` and generated `.lock.yml` files

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines and how to add a new plugin.

## License

See [LICENSE](LICENSE) for details.
