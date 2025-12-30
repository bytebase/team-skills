# Bytebase Team Skills

A collection of Claude Code skills shared by the Bytebase team. These skills encode proven workflows, domain knowledge, and best practices to help Claude Code assist more effectively with Bytebase-specific tasks.

## What are Skills?

Skills are reusable prompts and workflows that extend Claude Code's capabilities. When a skill is installed, Claude Code can invoke it to follow established patterns for specific tasks like writing release notes, debugging issues, or following code review guidelines.

## Available Skills

| Skill | Description |
|-------|-------------|
| `write-release-notes` | Generate professional Bytebase release notes by analyzing git commits, checking Terraform impact, searching Linear for customer feedback, and following established conventions |

## Installation

You can install these skills in two ways: via the **marketplace** (recommended for discovery and updates) or as a **direct plugin**.

### Option 1: Install via Marketplace (Recommended)

The marketplace allows you to browse and install plugins, and receive updates when new skills are added.

```bash
# Step 1: Add the marketplace
/plugin marketplace add bytebase/team-skills

# Step 2: Install the plugin from the marketplace
/plugin install bytebase-team-skills@bytebase-team-skill-market
```

**Managing the marketplace:**

```bash
# List all configured marketplaces
/plugin marketplace list

# Update/refresh the marketplace to get latest plugins
/plugin marketplace update bytebase-team-skill-market

# Remove the marketplace
/plugin marketplace remove bytebase-team-skill-market
```

### Option 2: Install as Direct Plugin

If you prefer to install the plugin directly without using the marketplace:

```bash
# Install directly from GitHub
/plugin install bytebase/team-skills
```

Or using the full Git URL:

```bash
/plugin install https://github.com/bytebase/team-skills.git
```

**To install a specific version:**

```bash
/plugin install https://github.com/bytebase/team-skills.git#v1.0.0
```

## Usage

Once installed, skills are automatically available to Claude Code. You can invoke a skill by name:

```bash
# Example: Generate release notes
/write-release-notes
```

Claude Code will also proactively use relevant skills when it detects a matching task.

## Verifying Installation

Check that the plugin is installed:

```bash
/plugin list
```

## Uninstalling

```bash
# Remove the plugin
/plugin uninstall bytebase-team-skills

# If using marketplace, you can also remove the marketplace
/plugin marketplace remove bytebase-team-skill-market
```

## Contributing

To add a new skill:

1. Create a new directory under `skills/` with your skill name
2. Add a `SKILL.md` file with the skill definition (frontmatter + content)
3. Submit a pull request

See existing skills for examples of the expected format.

## License

MIT
