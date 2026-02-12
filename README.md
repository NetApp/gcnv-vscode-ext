# Google Cloud NetApp Volumes VS Code Extension

**AI-Powered Storage Management for Developers**

A VS Code extension that brings Google Cloud NetApp Volumes (GCNV) storage management directly into your development environment. Manage storage resources, generate templates, and get AI-powered recommendations without leaving VS Code.

[![VS Code Marketplace](https://img.shields.io/badge/VS%20Code-Marketplace-blue)](https://marketplace.visualstudio.com/items?itemName=NetApp.gcnv-vscode-extension)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://github.com/NetApp/gcnv-vscode-ext/blob/main/LICENSE)
[![Version](https://img.shields.io/badge/Version-1.0.0-orange)](https://marketplace.visualstudio.com/items?itemName=netapp.google-cloud-netapp-volumes)

---

**The Solution:** AI-powered storage management integrated directly into VS Code with natural language commands and intelligent recommendations.

## ✨ Key Features

### AI-Powered Chat Integration
- **@gcnv Chat Participant**: Natural language storage management through GitHub Copilot, backed by **MCP (Model Context Protocol)** tool integration so the AI can list volumes, pools, networks, get metrics, and run other GCNV operations in real time
- **Intelligent Recommendations**: AI-powered analysis and optimization suggestions
- **Context-Aware Assistance**: Framework-specific code generation and best practices

### Core Functionality
- **Resource Management**: Browse and manage GCNV projects, capacity pools, and volumes
- **Template Generation**: Create Terraform templates with AI assistance
- **One-Click Operations**: Generate mount scripts, and deploy templates
- **Real-Time Analysis**: Performance metrics and cost optimization insights

### Developer/Devops Experience
- **Zero Context Switching**: Everything happens in VS Code

### Natural Language Commands & MCP Integration

The extension uses **MCP (Model Context Protocol)** integration so the AI can call GCNV tools on your behalf. When you use the **@gcnv** chat participant, your requests are fulfilled by a mix of **MCP tools** (for discovery and live data) and **direct API calls** (for analysis and actions).

#### How It Works

- **MCP tools** – The chat participant can invoke tools such as `gcnv_list_volumes`, `gcnv_list_pools`, `gcnv_get_metrics`, and others to fetch real-time data from your GCP project.
- **Direct API + context** – For the selected resource in the explorer, the extension uses direct API calls and collected context for analysis, templates, and mount scripts.

**Flow:** Chat request → GCNV Chat Participant → MCP service (tool execution) or direct API → GCNVService → Google Cloud APIs → Response in chat.

#### Natural Language Commands (Examples)

**Discovery (no resource selection; uses MCP tools):**
- *"List all volumes"* / *"Show all storage pools"* / *"List all networks"*
- *"What projects do I have?"* / *"List available regions"*
- *"Get metrics for volume &lt;volume-name&gt;"* / *"Check peering for network &lt;network-name&gt;"*

**Resource-specific (select a volume or pool in GCNV Explorer first):**
- *"Analyze this volume"* / *"Analyze this pool"*
- *"Generate Terraform template for this volume"* / *"Generate mount script for this volume"*
- *"Optimize this pool"* / *"What can you tell me about this resource?"*

**Utility:**
- *"Show me our conversation history"* / *"Clear history"*

#### MCP Tool Categories (Summary)

| Category | Example tools | Use for |
|----------|----------------|--------|
| **Volumes** | `gcnv_list_volumes`, `gcnv_get_volume` | List/get volumes |
| **Storage Pools** | `gcnv_list_pools`, `gcnv_get_pool` | List/get pools |
| **Snapshots** | `gcnv_snapshot_list`, `gcnv_snapshot_create` | List/create snapshots |
| **Networks** | `gcnv_list_networks`, `gcnv_get_peering` | Networks and peering |
| **Projects & Regions** | `gcnv_get_projects`, `gcnv_get_regions` | Projects and regions |
| **Performance** | `gcnv_get_metrics` | Volume metrics (throughput, latency, capacity) |

Open the chat (`Cmd+L` / `Ctrl+L`), select the **gcnv** participant, and use the commands above. For analysis, template generation, or mount scripts, select the volume or pool in the GCNV Explorer first.

## Prerequisites

- **VS Code**: Version 1.77.0 or higher
- **Google Cloud Account**: With access to GCNV
- **API Enablement and IAM Permissions**: Google API, Google compute API and Cloud Resource Manager API enabled under “APIs & Services”. Under “IAM & Admin / IAM” in Google Cloud, your email has “Owner” and “Service Usage Admin” roles
- **GitHub Copilot**: For AI-powered chat and MCP-backed natural language commands (optional but recommended)

## Installation

### From VS Code Marketplace

1. Open VS Code
2. Go to Extensions (`Ctrl+Shift+X` / `Cmd+Shift+X`)
3. Search for "Google Cloud NetApp Volumes"
4. Click **Install**

## Security Disclosures

This extension requires access to your Google Cloud account to manage Google Cloud NetApp Volumes resources.

**Information We Access:**
- Google Account Email - to identify the authenticated user
- Google Cloud Projects - to list and display your GCNV resources  
- GCNV Resources - to display and manage your volumes, pools, and snapshots

**Data Storage:**
All authentication tokens are stored securely in VS Code's secret storage on your local machine. We do not transmit or store your data on external servers.

**Third-Party Services:**
This extension communicates directly with Google Cloud APIs. No data is sent to NetApp servers.

For more information, see [Google Cloud Privacy Policy](https://cloud.google.com/terms/cloud-privacy-notice).
