# 🔌 Highlite Plugin Hub
**As of 9/18/2025 Highl1te Development has been paused indefinitely**

A centralized repository for managing and distributing Highlite plugins.

## 📋 Table of Contents

- [Overview](#overview)
- [Creating a Plugin](#creating-a-plugin)
- [Adding a Plugin to the Hub](#adding-a-plugin-to-the-hub)
- [Updating a Plugin](#updating-a-plugin)
- [Plugin Configuration](#plugin-configuration)
- [Contributing](#contributing)
- [Support](#support)

## 🎯 Overview

The Highlite Plugin Hub serves as the official registry for Highlite plugins. It provides:

- **Automated Distribution**: Seamless plugin installation and updates
- **Version Management**: Track and manage plugin versions

## 🛠️ Creating a Plugin

Ready to build your own plugin? We've got you covered!

📖 **Comprehensive Guide**: Follow our detailed step-by-step instructions at:
👉 **https://github.com/Highl1te/Example-Plugin/**

The example repository includes:
- Complete plugin template
- Development setup instructions
- Best practices and coding standards
- Testing guidelines
- Release process documentation

## 📦 Adding a Plugin to the Hub

To make your plugin available through the Plugin Hub:

### Step 1: Prepare Your Plugin
1. Ensure your plugin follows the [plugin development guidelines](https://github.com/Highl1te/Example-Plugin/)
2. Create a release in your plugin repository
3. Note the SHA hash of your release asset

### Step 2: Add to Plugin Hub
1. **Fork this repository**
2. **Create a new JSON file** in the `plugins/` directory:
   ```
   plugins/your-plugin-name.json
   ```
3. **Configure your plugin** using this template:
   ```json
   {
       "repository_owner": "YOUR_GITHUB_USERNAME",
       "repository_name": "YOUR_PLUGIN_REPO_NAME",
       "asset_sha": "sha256:YOUR_RELEASE_ASSET_SHA"
   }
   ```
4. **Submit a Pull Request** with your changes

### Step 3: Get Your Asset SHA
The `asset_sha` is required for security and version tracking:

1. Go to your plugin's GitHub releases page
2. Find the release you want to distribute
3. Click on the release asset (typically `PluginName.js`)
4. Copy the SHA256 hash from the asset details
5. Format it as: `sha256:YOUR_HASH_HERE`

## 🔄 Updating a Plugin

When you release a new version of your plugin:

1. **Find your plugin file**: Locate `plugins/your-plugin-name.json`
2. **Update the asset SHA**: Change the `asset_sha` field to point to your new release
3. **Submit a Pull Request**: Include a brief description of what's new

### Example Update
```json
{
    "repository_owner": "YourUsername",
    "repository_name": "AwesomePlugin",
    "asset_sha": "sha256:NEW_SHA_HASH_FOR_LATEST_RELEASE"
}
```

## ⚙️ Plugin Configuration

### Required Fields

| Field | Type | Description |
|-------|------|-------------|
| `repository_owner` | string | GitHub username or organization name |
| `repository_name` | string | Name of the plugin repository |
| `asset_sha` | string | SHA256 hash of the release asset (prefixed with `sha256:`) |

### File Naming Convention
- Use kebab-case for plugin file names
- Example: `my-awesome-plugin.json`
- Keep names descriptive but concise

## 🤝 Contributing

We welcome contributions to improve the Plugin Hub! Here's how you can help:

### For Plugin Developers
- Submit your plugins following the guidelines above
- Keep your plugin information up to date
- Report any issues with the distribution process

### For Hub Improvements
- Report bugs or suggest features via [GitHub Issues](https://github.com/Highl1te/Plugin-Hub/issues)
- Submit Pull Requests for documentation improvements
- Help review plugin submissions

### Guidelines
- Follow the existing file structure and naming conventions
- Test your changes before submitting
- Include clear commit messages
- Be respectful and collaborative

## 🆘 Support

Need help? We're here for you!

- **Plugin Development**: Check the [Example Plugin repository](https://github.com/Highl1te/Example-Plugin/)
- **Hub Issues**: Create an issue in this repository
- **General Questions**: Reach out on Discord!

## 📄 License

This project is licensed under the terms specified in the [LICENSE](LICENSE) file.
