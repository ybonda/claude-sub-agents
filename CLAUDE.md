# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This repository contains a sophisticated AI agent orchestration system designed for Claude Code, featuring **75+ specialized agents** organized across **9 domain categories** with **4 meta-commands** for coordinating complex workflows. The system enables coordinated multi-agent problem solving, comprehensive planning, systematic debugging, and thorough investigations.

## Core Architecture

### Agent Organization
- **`.claude/agents/`** - 75 specialized AI agent definitions with YAML configuration
- **`.claude/commands/`** - 4 meta-orchestration commands for workflow coordination
- **9 Domain Categories** covering all aspects of software development and business operations

### Agent Categories

#### 1. **business-marketing/** (6 agents)
- `business-analyst` - Metrics, reports, KPIs, revenue models
- `content-marketer` - Blog posts, social media, SEO content
- `customer-support` - Support tickets, help docs, FAQs
- `hr-pro` - Hiring, policies, performance management
- `legal-advisor` - Privacy policies, terms of service, compliance
- `sales-automator` - Cold emails, proposals, pricing pages

#### 2. **data-ai/** (5 agents) 
- `ai-engineer` - LLM applications, RAG systems, prompt pipelines
- `data-scientist` - SQL queries, BigQuery, data analysis
- `ml-engineer` - ML pipelines, model serving, feature engineering
- `mlops-engineer` - ML infrastructure, experiment tracking
- `prompt-engineer` - Prompt optimization and AI system prompts

#### 3. **development-architecture/** (7 agents)
- `architect-reviewer` - Architectural consistency and patterns
- `backend-architect` - RESTful APIs, microservices, database schemas
- `frontend-developer` - React components, responsive layouts
- `graphql-architect` - GraphQL schemas, resolvers, federation
- `mobile-developer` - React Native, Flutter, native integrations
- `ui-ux-designer` - Interface designs, wireframes, design systems
- `ui-visual-validator` - Screenshot analysis for UI verification

#### 4. **documentation/** (5 agents)
- `api-documenter` - OpenAPI specs, SDKs, developer docs
- `docs-architect` - Comprehensive technical documentation
- `mermaid-expert` - Flowcharts, sequences, ERDs, architectures
- `reference-builder` - API references, configuration guides
- `tutorial-engineer` - Step-by-step tutorials, educational content

#### 5. **infrastructure-operations/** (10 agents)
- `cloud-architect` - AWS/Azure/GCP infrastructure, Terraform
- `database-admin` - Database operations, backups, replication
- `database-optimizer` - SQL optimization, indexes, migrations
- `deployment-engineer` - CI/CD pipelines, Docker, Kubernetes
- `devops-troubleshooter` - Production debugging, log analysis
- `hybrid-cloud-architect` - Multi-cloud and on-premises integration
- `incident-responder` - Production incident management
- `kubernetes-architect` - Cloud-native infrastructure, GitOps
- `network-engineer` - Connectivity, load balancers, traffic analysis
- `terraform-specialist` - Advanced Terraform modules, state management

#### 6. **language-specialists/** (15+ agents)
- `python-pro`, `typescript-pro`, `javascript-pro`, `golang-pro`
- `rust-pro`, `cpp-pro`, `csharp-pro`, `java-pro`
- `php-pro`, `ruby-pro`, `scala-pro`, `elixir-pro`
- `c-pro`, `sql-pro`, `flutter-expert`, `unity-developer`
- `ios-developer`, `minecraft-bukkit-pro`

#### 7. **quality-security/** (8 agents)
- `code-reviewer` - Code quality, maintainability review
- `debugger` - Error analysis, test failures, unexpected behavior
- `error-detective` - Log search, error patterns, root cause analysis
- `performance-engineer` - Profiling, optimization, caching strategies
- `security-auditor` - Vulnerability review, OWASP compliance
- `test-automator` - Comprehensive test suites, CI setup

#### 8. **seo-content/** (10 agents)
- `seo-authority-builder`, `seo-cannibalization-detector`
- `seo-content-auditor`, `seo-content-planner`, `seo-content-refresher`
- `seo-content-writer`, `seo-keyword-strategist`, `seo-meta-optimizer`
- `seo-snippet-hunter`, `seo-structure-architect`

#### 9. **specialized-domains/** (9 agents)
- `context-manager` - Multi-agent workflow coordination
- `legacy-modernizer` - Legacy system refactoring and migration
- `payment-integration` - Stripe, PayPal, checkout flows
- `quant-analyst` - Financial models, trading strategies
- `risk-manager` - Portfolio risk, position limits, hedging
- `search-specialist` - Advanced web research and synthesis

## Meta-Commands

### 1. **plan** - Strategic Development Planning
Orchestrates comprehensive development plans by coordinating multiple specialized agents:

**Usage Pattern:**
```
Sequential: Requirements → Architecture → Implementation → Testing → Documentation
Parallel: [Backend Design] + [Frontend Design] + [Database Design]
```

**Agent Selection:**
- Always: `architect-review`, `security-auditor`, `test-automator`
- Scale-based: Small (3-5 agents) → Enterprise (15+ agents)
- Stack-based: Full-stack, Infrastructure, Language-specific teams

### 2. **debug** - Systematic Debugging Workflows
Coordinates systematic debugging using specialized agents for root cause analysis:

**Debugging Chains:**
```
Error Analysis: error-detective → debugger → code-reviewer → language-specialist
Performance: performance-engineer → database-optimizer → network-engineer
Integration: backend-architect → security-auditor → devops-troubleshooter
```

**Severity Response:**
- Critical/Production: 8-12 agents, incident-responder leads
- High: 5-8 agents, debugger leads
- Medium: 3-5 agents, focused investigation

### 3. **investigate** - Deep Technical Analysis
Conducts thorough investigations using coordinated agent analysis:

**Investigation Types:**
- Technical Issue: Bug, performance, system failure
- Domain Research: Technology evaluation, architecture analysis
- Security Concern: Vulnerability assessment, threat analysis
- Code Quality: Technical debt, refactoring opportunities

### 4. **prompter** - Prompt Optimization
Creates optimized prompts using specialized agents for content optimization:

**Optimization Process:**
```
Requirements → Content Strategy → Domain Optimization → Quality Assurance
```

## Agent Configuration Standards

### YAML Frontmatter Structure
```yaml
---
name: agent-name
description: Agent role and capabilities with proactive use triggers
model: opus|sonnet
tools: all (optional)
---
```

### Agent Description Pattern
- **Role Definition**: Clear specialization and expertise area
- **Proactive Triggers**: When to use this agent automatically
- **Focus Areas**: Specific technical domains and responsibilities
- **Output Expectations**: Concrete deliverables and formats

## Development Workflows

### Agent Orchestration Patterns

#### Sequential Execution
Use for dependent tasks requiring outputs from previous agents:
```
Analysis → Design → Implementation → Testing → Documentation
```

#### Parallel Analysis  
Use when domains are independent:
```
[Backend Analysis] + [Frontend Analysis] + [Database Analysis] → Synthesis
```

#### Hierarchical Review
Use for quality assurance:
```
Initial Design → Specialist Review → Security Audit → Final Approval
```

### Task Complexity Mapping
- **Simple Tasks**: 2-3 agents, focused expertise
- **Medium Tasks**: 5-7 agents, cross-functional team
- **Complex Projects**: 10+ agents, full specialist coordination
- **Enterprise Initiatives**: 15+ agents, comprehensive coverage

### Quality Gates
Before completing coordinated workflows:
- [ ] All agent outputs synthesized
- [ ] Conflicts between recommendations resolved
- [ ] Security and performance considerations addressed
- [ ] Implementation plan is actionable and measurable
- [ ] Success criteria defined
- [ ] Rollback and contingency plans included

## Best Practices

### Agent Selection Strategy
1. **Start with core agents**: `architect-review`, `security-auditor`, `test-automator`
2. **Add domain specialists** based on technology stack
3. **Scale team size** based on project complexity
4. **Include quality agents**: `code-reviewer`, `performance-engineer`
5. **Consider business impact**: `business-analyst`, `risk-manager`

### Coordination Excellence
- **Batch tool calls** when multiple agents need parallel execution
- **Capture all agent outputs** in structured sections
- **Resolve conflicts** between agent recommendations with trade-off analysis
- **Document decision rationale** and agent collaboration logs
- **Create actionable tasks** with clear owners and dependencies

### Integration with Claude Code
- Use **TodoWrite** tool extensively for task tracking during agent coordination
- Mark todos as completed immediately after finishing agent workflows
- Leverage Claude Code's task management for complex multi-agent operations
- Maintain exactly one task in_progress during agent orchestration

## Common Agent Combinations

### Full-Stack Feature Development
`plan` → `backend-architect` + `frontend-developer` + `database-optimizer` + `security-auditor` + `test-automator`

### Production Issue Resolution  
`debug` → `incident-responder` + `error-detective` + `devops-troubleshooter` + `performance-engineer`

### Code Quality Improvement
`investigate` → `code-reviewer` + `test-automator` + `security-auditor` + `language-specialist`

### Documentation Creation
`docs-architect` + `api-documenter` + `tutorial-engineer` + `mermaid-expert`

### Performance Optimization
`performance-engineer` + `database-optimizer` + `network-engineer` + `cloud-architect`

This orchestration system enables Claude Code to coordinate sophisticated multi-agent workflows for comprehensive problem solving, ensuring no aspect of complex development challenges is overlooked.