# Google Cloud NetApp Volumes VS Code Extension

**AI-Powered Storage Management for Developers**

A VS Code extension that brings Google Cloud NetApp Volumes (GCNV) storage management directly into your development environment. Manage storage resources, generate templates, and get AI-powered recommendations without leaving VS Code.

[![VS Code Marketplace](https://img.shields.io/visual-studio-marketplace/v/netapp.azure-netapp-files)](https://marketplace.visualstudio.com/items?itemName=netapp.azure-netapp-files)
[![License](https://img.shields.io/github/license/NetApp/anf-vscode-extension)](https://github.com/NetApp/anf-vscode-extension/blob/main/LICENSE)
[![Version](https://img.shields.io/visual-studio-marketplace/v/netapp.azure-netapp-files)](https://marketplace.visualstudio.com/items?itemName=netapp.azure-netapp-files)

---

**The Solution:** AI-powered storage management integrated directly into VS Code with natural language commands and intelligent recommendations.

## ✨ Key Features

### AI-Powered Chat Integration
- **@anf Chat Participant**: Natural language storage management through GitHub Copilot
- **Intelligent Recommendations**: AI-powered analysis and optimization suggestions
- **Context-Aware Assistance**: Framework-specific code generation and best practices

### Core Functionality
- **Resource Management**: Browse and manage ANF accounts, capacity pools, and volumes
- **Template Generation**: Create ARM, Terraform, and Powershell templates with AI assistance
- **One-Click Operations**: Copy connection strings, generate mount scripts, and deploy templates
- **Real-Time Analysis**: Performance metrics and cost optimization insights

### Developer/Devops Experience
- **Zero Context Switching**: Everything happens in VS Code
- **Natural Language Commands**: "analyze this volume", "generate ARM template", "optimize configuration"
- **Framework Integration**: Direct code insertion for .NET, Python, Java, Node.js

## Prerequisites

- **VS Code**: Version 1.77.0 or higher
- **Azure Account**: With access to Azure NetApp Files
- **Azure Subscription**: With ANF service enabled
- **Permissions**: Contributor or NetApp Contributor role on target subscriptions
- **GitHub Copilot**: For AI-powered chat features (optional but recommended)

## Installation

### From VS Code Marketplace

1. Open VS Code
2. Go to Extensions (`Ctrl+Shift+X` / `Cmd+Shift+X`)
3. Search for "Azure NetApp Files"
4. Click **Install**

### From Source

```bash
git clone https://github.com/NetApp/anf-vscode-extension.git
cd anf-vscode-extension
npm install
npm run compile
