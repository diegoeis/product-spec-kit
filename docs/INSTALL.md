# Installation Guide - Product Spec Kit v2.0

Complete installation instructions for all platforms.

---

## Prerequisites

- **Claude Desktop** installed (Mac, Windows, or Linux)
- **Access** to your file system
- **Terminal/Command Prompt** access

---

## Installation Methods

### Method 1: Manual Installation (Recommended)

#### macOS / Linux

```bash
# 1. Create skills directory if it doesn't exist
mkdir -p ~/.config/claude/skills/user/

# 2. Extract the ZIP
unzip product-spec-kit-v2.0.zip

# 3. Copy to Claude skills directory
cp -r product-spec-kit-v2 ~/.config/claude/skills/user/product-spec-kit

# 4. Verify structure
ls -la ~/.config/claude/skills/user/product-spec-kit
```

#### Windows

```powershell
# 1. Create skills directory if it doesn't exist
New-Item -ItemType Directory -Force -Path "$env:APPDATA\Claude\skills\user"

# 2. Extract the ZIP to a temporary location
# (Use Windows Explorer or 7-Zip)

# 3. Copy to Claude skills directory
Copy-Item -Path ".\product-spec-kit-v2" -Destination "$env:APPDATA\Claude\skills\user\product-spec-kit" -Recurse

# 4. Verify structure
Get-ChildItem "$env:APPDATA\Claude\skills\user\product-spec-kit"
```

---

## Verification

### Step 1: Restart Claude Desktop

- **macOS**: Quit Claude Desktop (Cmd+Q) and reopen
- **Windows**: Exit Claude Desktop and reopen
- **Linux**: Close and reopen Claude Desktop

### Step 2: Test Installation

Open a new conversation in Claude and say:

```
"Do I have Product Spec Kit installed?"
```

Claude should respond confirming the skill is available.

### Step 3: Verify Files

Expected structure:

```
~/.config/claude/skills/user/product-spec-kit/
├── SKILL.md
├── README.md
├── CHANGELOG.md
├── templates/
│   ├── prd-template.md
│   ├── plan-template.md
│   ├── stories-template.md
│   ├── quick-issue-template.md
│   └── checklist-template.md
├── memory/
│   └── constitution.md
├── examples/
└── docs/
    ├── QUICKSTART.md
    ├── INSTALL.md (this file)
    ├── WORKFLOWS.md
    ├── INDEX.md
    └── STRUCTURE.md
```

---

## Common Installation Issues

### Issue 1: Skill Not Found

**Symptom**: Claude says "I don't have that skill installed"

**Solutions**:
1. Check file path is correct
2. Ensure folder name is exactly `product-spec-kit`
3. Restart Claude Desktop
4. Check permissions on the directory

**macOS/Linux**:
```bash
chmod -R 755 ~/.config/claude/skills/user/product-spec-kit
```

**Windows**: Ensure your user has read permissions on the directory

---

### Issue 2: Files Missing

**Symptom**: Some templates or files not loading

**Solution**:
```bash
# Re-extract and copy all files
unzip -o product-spec-kit-v2.0.zip
cp -r product-spec-kit-v2/* ~/.config/claude/skills/user/product-spec-kit/
```

---

### Issue 3: Wrong Directory

**Common mistakes**:
- ❌ `~/.config/claude/skills/product-spec-kit` (missing `/user/`)
- ❌ `~/.config/claude/product-spec-kit` (missing `/skills/user/`)
- ✅ `~/.config/claude/skills/user/product-spec-kit` (correct!)

---

### Issue 4: Permission Denied

**macOS/Linux**:
```bash
# Fix permissions
sudo chown -R $USER:$USER ~/.config/claude/skills/user/product-spec-kit
chmod -R 755 ~/.config/claude/skills/user/product-spec-kit
```

---

## MCP Configuration (Optional)

For repository integration, you need MCP Filesystem configured.

### macOS Configuration

Edit `~/Library/Application Support/Claude/claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/path/to/your/projects"
      ]
    }
  }
}
```

### Windows Configuration

Edit `%APPDATA%\Claude\claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "C:\\path\\to\\your\\projects"
      ]
    }
  }
}
```

**After configuration**: Restart Claude Desktop

---

## Updating from v1.0 to v2.0

### Backup First

```bash
# Backup existing installation
cp -r ~/.config/claude/skills/user/product-spec-kit ~/.config/claude/skills/user/product-spec-kit.backup
```

### Update

```bash
# Extract new version
unzip product-spec-kit-v2.0.zip

# Replace old version
rm -rf ~/.config/claude/skills/user/product-spec-kit
cp -r product-spec-kit-v2 ~/.config/claude/skills/user/product-spec-kit

# Restart Claude Desktop
```

### Verify Update

```
"What version of Product Spec Kit do I have?"
```

Should respond: v2.0

---

## Uninstallation

### Remove Skill

**macOS/Linux**:
```bash
rm -rf ~/.config/claude/skills/user/product-spec-kit
```

**Windows**:
```powershell
Remove-Item -Path "$env:APPDATA\Claude\skills\user\product-spec-kit" -Recurse -Force
```

### Restart Claude Desktop

---

## Multi-User Installation

For teams wanting to standardize on this skill:

### Option 1: Shared Installation Instructions

1. Distribute the ZIP file
2. Provide this installation guide
3. Each user installs individually

### Option 2: Configuration Management

For enterprise environments, use configuration management tools to:
1. Deploy ZIP to user machines
2. Extract to correct location
3. Set permissions
4. Restart Claude Desktop

---

## Troubleshooting Installation

### Check Installation Location

**macOS/Linux**:
```bash
ls -la ~/.config/claude/skills/user/product-spec-kit/SKILL.md
```

Should show the SKILL.md file.

**Windows**:
```powershell
Test-Path "$env:APPDATA\Claude\skills\user\product-spec-kit\SKILL.md"
```

Should return `True`.

---

### Verify File Contents

```bash
# Check main skill file exists and is readable
head -n 5 ~/.config/claude/skills/user/product-spec-kit/SKILL.md
```

Should show the beginning of the SKILL.md file.

---

### Claude Logs

If issues persist, check Claude logs:

**macOS**:
```bash
tail -f ~/Library/Logs/Claude/app.log
```

**Windows**:
```powershell
Get-Content "$env:APPDATA\Claude\logs\app.log" -Tail 50
```

Look for skill loading errors.

---

## Getting Help

If installation problems persist:

1. **Double-check paths**: Ensure exact directory structure
2. **Check permissions**: Files must be readable
3. **Restart Claude**: Always restart after changes
4. **Verify ZIP**: Re-download if corrupt
5. **Check version**: Ensure Claude Desktop is up to date

---

## Post-Installation

Once installed successfully:

1. Read [QUICKSTART.md](QUICKSTART.md) for first steps
2. Review [WORKFLOWS.md](WORKFLOWS.md) for detailed guides
3. Check [constitution.md](../memory/constitution.md) for principles
4. Try creating your first quick story!

---

## System Requirements

- **Claude Desktop**: Latest version recommended
- **Disk Space**: ~1 MB
- **OS**: macOS 10.15+, Windows 10+, or Linux (modern distro)
- **Node.js**: Only required if using MCP Filesystem (optional)

---

**Installation complete?** Head to [QUICKSTART.md](QUICKSTART.md)! 🚀
