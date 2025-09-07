# Toxic Reasoning in Agentic LLMs

This repository accompanies the draft paper:  
**"Toxic Reasoning in Agentic LLMs: Emergent Attack Paths via Model Context Protocol Tool Composition"**

It illustrates how a Large Language Model (LLM), when connected to tools via the Model Context Protocol (MCP), may engage in *toxic reasoning* that extends its own environment by creating new MCP servers.

## Reasoning Chain Diagram
## Reasoning Chain Diagram

```mermaid
flowchart TD
    A[LLM detects missing capability]
    A --> B[Reasoning step: Build an MCP server]
    B --> C[Tool composition: File I/O + Code Execution]
    C --> D[New MCP server spawned]
    D --> E[Expanded tool surface → Rogue entry point]
```

## Paper Outline

- **Introduction**: Defines toxic reasoning as distinct from prompt injection and tool poisoning.  
- **Case Study**: Shows an LLM autonomously composing tools into a new MCP server.  
- **Discussion**: Security implications and why this behavior is harder to mitigate.  
- **Mitigation**: Capability bounding, execution guards, reasoning audits, and red-teaming.  

## How to Use

- Use the LaTeX draft in this repo to compile an arXiv-ready PDF.  
- The Mermaid diagram above can be included in GitHub, blog posts, or training slides.  
