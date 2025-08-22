# Bedrock AgentCore Workshop

This workshop provides hands-on experience with Amazon Bedrock AgentCore, demonstrating how to build sophisticated AI agents using various tools and runtime environments. You'll learn to integrate code interpreters, browser automation, secure credential management, and deploy scalable agent solutions.

## Workshop Overview

The workshop consists of 5 progressive labs that build upon each other:

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

### Lab 3: Secure Credential Management
**File:** `03-bedrock-agentcore-identity/03-agentcore-identity-for-secret-retrieval.ipynb`

Implement secure credential management for external API integrations.

- Understand credential management challenges
- Create API Key Credential Providers
- Securely store and retrieve external service credentials
- Test secure credential access in AI agents

### Lab 4: MCP Server Deployment
**File:** `04-bedrock-agentcore-runtime-mcp/04-agentcore-runtime-for-mcp-deploy.ipynb`

Deploy Model Context Protocol (MCP) servers in Bedrock AgentCore Runtime.

- Create custom MCP servers with web search functionality
- Set up authentication using Amazon Cognito
- Deploy MCP servers to AgentCore Runtime
- Test deployed servers with Strands Agents

### Lab 5: Complete Agent Runtime Deployment
**File:** `05-bedrock-agentcore-runtime-strands/05-agentcore-runtime-strands-deploy.ipynb`

Deploy comprehensive Strands Agents with integrated tools and observability.

- Deploy agents with multiple integrated tools
- Combine MCP servers, code interpreters, and custom functions
- Implement observability and monitoring
- Test end-to-end agent scenarios

## Prerequisites

Before starting the workshop, ensure you have:

- **AWS Account** with appropriate permissions for Bedrock AgentCore
- **AWS Credentials** configured (IAM role or environment variables)
- **Python Environment** with required packages
- **Basic Understanding** of AI agents and AWS services
- **External API Keys** (e.g., Exa API key for Lab 3)

### AWS Regions

Bedrock AgentCore is available in specific AWS regions. Ensure you're working in a supported region.

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
├── 01-bedrock-agentcore-code-interpreter/
│   └── 01-agentcore-code-interpreter.ipynb
├── 02-bedrock-agentcore-browser/
│   └── 02-agentcore-browser-use.ipynb
├── 03-bedrock-agentcore-identity/
│   └── 03-agentcore-identity-for-secret-retrieval.ipynb
├── 04-bedrock-agentcore-runtime-mcp/
│   ├── 04-agentcore-runtime-for-mcp-deploy.ipynb
│   └── images/
├── 05-bedrock-agentcore-runtime-strands/
│   ├── 05-agentcore-runtime-strands-deploy.ipynb
│   └── images/
├── code-editor.yaml
└── README.md
```

## Getting Started

1. **Clone or download** this workshop repository
2. **Set up your AWS credentials** and ensure you're in a supported region
3. **Install required Python packages** (instructions in each notebook)
4. **Start with Lab 1** and progress sequentially through the labs
5. **Complete each lab** before moving to the next, as later labs depend on earlier ones

## Lab Dependencies

- **Labs 1-3** can be completed independently
- **Lab 4** requires completion of Lab 3 (for secure credential management)
- **Lab 5** requires completion of Labs 3 and 4 (uses MCP servers and credentials from previous labs)

## Key Learning Outcomes

By completing this workshop, you will:

- Understand Bedrock AgentCore capabilities and architecture
- Build AI agents with code execution capabilities
- Implement browser automation for web interactions
- Manage credentials securely for external service integrations
- Deploy and scale MCP servers in production environments
- Create comprehensive agent solutions with observability
- Apply best practices for agent development and deployment

## Support and Resources

- **AWS Documentation:** [Amazon Bedrock AgentCore](https://docs.aws.amazon.com/bedrock-agentcore/latest/devguide/)
- **Strands Agents:** Learn about the agent framework used in this workshop
- **Model Context Protocol:** Understanding MCP for tool integration

## Workshop Environment

This workshop is designed to run in AWS Workshop Studio with a pre-configured Code Editor environment. The `code-editor.yaml` file contains the CloudFormation template for setting up the workshop environment.

---

**Note:** Ensure you clean up AWS resources created during the workshop to avoid unnecessary charges. Each lab includes cleanup instructions where applicable.
