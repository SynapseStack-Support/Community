# GitHub Labels Configuration for SynapseStack

## 📋 Recommended Labels

Copy and paste these labels into your GitHub repository settings:

### Issue Types
| Label | Color | Description |
|-------|-------|-------------|
| `bug` | `#d73a4a` | Something isn't working |
| `enhancement` | `#a2eeef` | New feature or request |
| `question` | `#d876e3` | Further information is requested |
| `support` | `#0075ca` | User needs help or guidance |
| `documentation` | `#0075ca` | Improvements or additions to documentation |

### Priority Levels
| Label | Color | Description |
|-------|-------|-------------|
| `priority: critical` | `#b60205` | System broken, immediate attention needed |
| `priority: high` | `#d93f0b` | Important issue, needs attention soon |
| `priority: medium` | `#fbca04` | Standard priority |
| `priority: low` | `#0e8a16` | Nice to have, not urgent |

### Status Labels
| Label | Color | Description |
|-------|-------|-------------|
| `status: triage` | `#ededed` | Needs initial review and categorization |
| `status: investigating` | `#f9d0c4` | Looking into the issue |
| `status: in-progress` | `#c2e0c6` | Actively working on this |
| `status: waiting-for-info` | `#fef2c0` | Waiting for more information from user |
| `status: duplicate` | `#cfd3d7` | This issue already exists |
| `status: wont-fix` | `#ffffff` | Valid issue but won't be addressed |

### Component Labels
| Label | Color | Description |
|-------|-------|-------------|
| `component: installation` | `#1d76db` | Installation and setup issues |
| `component: configuration` | `#1d76db` | Configuration and settings |
| `component: web-ui` | `#1d76db` | Web interface problems |
| `component: containers` | `#1d76db` | Container management (Podman/Docker) |
| `component: ai-models` | `#1d76db` | Ollama and AI model issues |
| `component: monitoring` | `#1d76db` | Performance monitoring and metrics |
| `component: backup` | `#1d76db` | Backup and recovery functionality |
| `component: security` | `#1d76db` | Security and authentication |
| `component: api` | `#1d76db` | REST API issues |

### Platform Labels
| Label | Color | Description |
|-------|-------|-------------|
| `platform: ubuntu` | `#5319e7` | Ubuntu/Debian systems |
| `platform: rhel` | `#5319e7` | RHEL/CentOS/Rocky Linux |
| `platform: arch` | `#5319e7` | Arch Linux |
| `platform: windows` | `#5319e7` | Windows (if supported) |

### Hardware Labels  
| Label | Color | Description |
|-------|-------|-------------|
| `hardware: gpu-nvidia` | `#006b75` | NVIDIA GPU related |
| `hardware: gpu-amd` | `#006b75` | AMD GPU related |
| `hardware: cpu-only` | `#006b75` | CPU-only deployment |

## 🚀 Quick Setup Script

You can use GitHub CLI to create these labels automatically:

```bash
# Install GitHub CLI first: https://cli.github.com/

# Issue Types
gh label create "bug" --color "d73a4a" --description "Something isn't working"
gh label create "enhancement" --color "a2eeef" --description "New feature or request"  
gh label create "question" --color "d876e3" --description "Further information is requested"
gh label create "support" --color "0075ca" --description "User needs help or guidance"
gh label create "documentation" --color "0075ca" --description "Improvements or additions to documentation"

# Priority Levels
gh label create "priority: critical" --color "b60205" --description "System broken, immediate attention needed"
gh label create "priority: high" --color "d93f0b" --description "Important issue, needs attention soon"
gh label create "priority: medium" --color "fbca04" --description "Standard priority"
gh label create "priority: low" --color "0e8a16" --description "Nice to have, not urgent"

# Status Labels
gh label create "status: triage" --color "ededed" --description "Needs initial review and categorization"
gh label create "status: investigating" --color "f9d0c4" --description "Looking into the issue"
gh label create "status: in-progress" --color "c2e0c6" --description "Actively working on this"
gh label create "status: waiting-for-info" --color "fef2c0" --description "Waiting for more information from user"
gh label create "status: duplicate" --color "cfd3d7" --description "This issue already exists"
gh label create "status: wont-fix" --color "ffffff" --description "Valid issue but won't be addressed"

# Component Labels
gh label create "component: installation" --color "1d76db" --description "Installation and setup issues"
gh label create "component: configuration" --color "1d76db" --description "Configuration and settings"
gh label create "component: web-ui" --color "1d76db" --description "Web interface problems"
gh label create "component: containers" --color "1d76db" --description "Container management issues"
gh label create "component: ai-models" --color "1d76db" --description "Ollama and AI model issues"
gh label create "component: monitoring" --color "1d76db" --description "Performance monitoring and metrics"
gh label create "component: backup" --color "1d76db" --description "Backup and recovery functionality"
gh label create "component: security" --color "1d76db" --description "Security and authentication"
gh label create "component: api" --color "1d76db" --description "REST API issues"

# Platform Labels
gh label create "platform: ubuntu" --color "5319e7" --description "Ubuntu/Debian systems"
gh label create "platform: rhel" --color "5319e7" --description "RHEL/CentOS/Rocky Linux"
gh label create "platform: arch" --color "5319e7" --description "Arch Linux"

# Hardware Labels
gh label create "hardware: gpu-nvidia" --color "006b75" --description "NVIDIA GPU related"
gh label create "hardware: gpu-amd" --color "006b75" --description "AMD GPU related"
gh label create "hardware: cpu-only" --color "006b75" --description "CPU-only deployment"
```

## 🔄 Label Management Workflow

### For Solo Developer Workflow:

1. **New Issue** → Auto-labeled by template + `status: triage`
2. **Review** → Add component, platform, priority labels
3. **Working** → Change to `status: in-progress`
4. **Need Info** → Change to `status: waiting-for-info`
5. **Resolved** → Close issue (GitHub handles closed status)

### Suggested Automation Rules:

- Issues created from templates automatically get appropriate base labels
- Add `status: triage` to all new issues
- Critical/High priority issues can trigger email notifications
- Use project boards for visual issue management if needed