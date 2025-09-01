# Bedrock AgentCore Workshop

This workshop provides hands-on experience with Amazon Bedrock AgentCore, demonstrating how to build sophisticated AI agents using various tools and runtime environments. You'll learn to integrate code interpreters, browser automation, secure credential management, memory capabilities, and deploy scalable agent solutions.

## Workshop Overview

The workshop consists of 8 progressive labs that build upon each other:

### Lab 0: Getting Started with Strands Agents
**File:** `00-strands-agents/00-strands-agents-getting-started.ipynb`

Introduction to Strands Agents framework and basic agent creation.

- Learn Strands Agents fundamentals
- Create your first AI agent
- Use built-in tools like calculator
- Develop custom tools and integrate them with agents

### Lab 1: Code Interpreter Integration
**File:** `01-bedrock-agentcore-code-interpreter/01-agentcore-code-interpreter.ipynb`

Learn how to integrate Strands Agents with Bedrock AgentCore Code Interpreter for dynamic code execution capabilities.

- Test default Code Interpreter functionality
- Create custom Code Interpreter with network access
- Compare execution environments and limitations
- Execute Python code dynamically within AI agents

### Lab 2: Browser Automation
**File:** `02-bedrock-agentcore-browser/02-agentcore-browser-use.ipynb`

Explore browser automation capabilities for web interaction and data extraction.

- Integrate browser automation with Strands Agents
- Navigate websites programmatically
- Extract information from web pages
- Implement common browser automation use cases

### Lab 3: Secure Credential Management with Exa MCP
**File:** `03-bedrock-agentcore-identity-apikey/03-agentcore-identity-for-exa-mcp.ipynb`

Implement secure credential management for external API integrations using Exa search as an example.

- Understand credential management challenges
- Create API Key Credential Providers for Exa API
- Securely store and retrieve external service credentials
- Test secure credential access with Exa MCP server

### Lab 4: MCP Server Deployment
**File:** `04-bedrock-agentcore-runtime-mcp/04-agentcore-runtime-for-mcp-deploy.ipynb`

Deploy Model Context Protocol (MCP) servers in Bedrock AgentCore Runtime.

- Create custom MCP servers with web search functionality
- Set up inbound authentication using Amazon Cognito
- Deploy MCP server to AgentCore Runtime
- Test deployed MCP server with Strands Agents

### Lab 5: Agent Runtime Deployment with Observability
**File:** `05-bedrock-agentcore-runtime-and-observability/05-agentcore-runtime-for-strands-deploy.ipynb`

Deploy Strands Agents with built-in and custom tools to Bedrock AgentCore Runtime with comprehensive observability features.

- Deploy the Strands Agents with tools to Bedrock AgentCore Runtime
- Use `boto3` with IAM permission to invoke the deployed agent
- Understand the nature of Bedrock AgentCore Runtime session
- Learn about GenAI Observability and Traceability

### Lab 6: Memory Integration
**File:** `06-bedrock-agentcore-memory/06-agentcore-memory.ipynb`

Integrate persistent memory capabilities with Strands Agents using Bedrock AgentCore Memory.

- Understand memory concepts in AI agents
- Implement short-term and long-term memory
- Create memory-enabled agents for conversational continuity
- Test memory retrieval across sessions

### Lab 7: Gateway Integration with OpenAPI
**File:** `07-bedrock-agentcore-gateway-openapi/07-agentcore-gateway-for-exa-openapi.ipynb`

Use Bedrock AgentCore Gateway to automatically generate MCP servers from OpenAPI specifications.

- Create Cognito inbound authentication for gateway access
- Upload OpenAPI specifications to generate MCP server
- Configure API key credential providers for outbound authentication
- Test generated MCP server with Strands Agents

## Prerequisites

Before starting the workshop, ensure you have:

- **AWS Account** with appropriate permissions for Bedrock AgentCore and related services
- [Nova Pro Model Access](https://docs.aws.amazon.com/nova/latest/userguide/getting-started-console.html) request in Bedrock
- [Enable CloudWatch Transaction Search](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/observability-configure.html#observability-configure-builtin) for AgentCore Observability
- **AWS Credentials** configured (IAM role or environment variables)
- **Python Environment** with required packages (instructions in each notebook)
- **Exa API Key** (required for Labs 3 and 7) - Get one from [Exa Dashboard](https://dashboard.exa.ai/api-keys)

### AWS Regions

We suggest to use `us-east-1` for this workshop. Bedrock AgentCore is available in specific AWS regions. Ensure you're working in a supported region.

### Environment Setup

If not using an IAM role, configure your AWS credentials:

```python
import os

os.environ["AWS_ACCESS_KEY_ID"] = "<YOUR_ACCESS_KEY>"
os.environ["AWS_SECRET_ACCESS_KEY"] = "<YOUR_SECRET_KEY>"
os.environ["AWS_SESSION_TOKEN"] = "<OPTIONAL_SESSION_TOKEN>"
os.environ["AWS_REGION"] = "<AWS_REGION>"
```

## Workshop Structure

```
bedrock-agentcore-workshop/
├── 00-strands-agents/
│   └── 00-strands-agents-getting-started.ipynb
├── 01-bedrock-agentcore-code-interpreter/
│   └── 01-agentcore-code-interpreter.ipynb
├── 02-bedrock-agentcore-browser/
│   └── 02-agentcore-browser-use.ipynb
├── 03-bedrock-agentcore-identity-apikey/
│   └── 03-agentcore-identity-for-exa-mcp.ipynb
├── 04-bedrock-agentcore-runtime-mcp/
│   ├── 04-agentcore-runtime-for-mcp-deploy.ipynb
├── 05-bedrock-agentcore-runtime-and-observability/
│   ├── 05-agentcore-runtime-for-strands-deploy.ipynb
├── 06-bedrock-agentcore-memory/
│   ├── 06-agentcore-memory.ipynb
├── 07-bedrock-agentcore-gateway-openapi/
│   ├── 07-agentcore-gateway-for-exa-openapi.ipynb
│   └── exa-openapi-spec.yaml
├── pyproject.toml
├── uv.lock
└── README.md
```

## Getting Started

1. **Set up your AWS credentials** and ensure you're in a supported region
2. Setup workshop environment with **uv** - [Installing uv](https://docs.astral.sh/uv/getting-started/installation/)
   ```bash
   uv sync
   ```
3. **Start with Lab 0** and progress sequentially through the labs
4. **Complete each lab** to clean up AWS resources 

## Key Learning Outcomes

By completing this workshop, you will:

- Understand Strands Agents fundamentals and framework
- Build AI agents with code execution capabilities
- Implement browser automation for web interactions
- Manage credentials securely for external service integrations
- Deploy and scale MCP servers in production environments
- Create comprehensive agent solutions with observability
- Integrate persistent memory capabilities for conversational continuity
- Generate MCP servers from OpenAPI specifications using Gateway
- Apply best practices for agent development and deployment

## Support and Resources

- [Amazon Bedrock AgentCore](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/)
- [Strands Agents](https://strandsagents.com/latest/)

---

**Note:** Ensure you clean up AWS resources created during the workshop to avoid unnecessary charges. Each lab includes cleanup instructions where applicable.
