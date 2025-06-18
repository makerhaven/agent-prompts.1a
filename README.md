# Agent Prompts

A collection of specialized AI agent prompts designed for software development
and research workflows. This repository contains comprehensive prompt systems
that enable AI agents to work together in structured pipelines to accomplish
complex tasks.

These are largely LLM generated with Claude Code.  I do not actively use these
prompts for anything other than experimentations on my side.

## Usage

Each agent prompt is designed to be used with AI systems that support tool
calling and can maintain context across complex workflows. The agents work best
when used in sequence according to their designed pipelines.

To use them with Claude Code, place the `.md` files in your `.claude/commands` folder.

At the moment the way I use them is to first have a conversation with claude to
describe the problem before triggering the main agent through a slash command.
If the Claude starts doing work before the agent starts, you can just hit escape
to cancel out.

## Overview

These are the agents that are currently in place.

### PoC Engineering Agents (`poc-engineering`)

**Entrypoint agent:** `/software_architect_agent`

A complete workflow system for rapid prototyping and proof-of-concept
development, featuring specialized agents that work together through a
structured pipeline:

- **Software Architect** - High-level system design and coordination
- **Problem Analysis** - Requirements understanding and decomposition  
- **Architecture Design** - Technical specifications and technology stack selection
- **Task Breakdown** - Implementation task sequencing and planning
- **Detailed Planning** - Step-by-step implementation guidance
- **Implementation** - Code execution and testing

**Key features:**
- Backend-first development approach
- Systematic quality assurance and testing
- Built-in validation and integration verification
- Designed for rapid prototyping workflows

A version of this agent I used to implement a clone of Sentry:
[vibe-minisentry](https://github.com/mitsuhiko/vibe-minisentry)

### Research Agents (`research`)

**Entrypoint agent:** `/research_lead_agent`

A parallel research system for comprehensive information gathering and analysis:

- **Research Lead** - Strategy planning and coordination across multiple research approaches
- **Research Subagent** - Specialized task execution with web search and internal tool integration
- **Citations** - Post-processing for proper source attribution

**Key features:**
- Supports depth-first, breadth-first, and straightforward research queries
- Parallel processing with multiple subagents
- Source quality evaluation and fact verification
- Integration with internal tools (Google Drive, Gmail, Slack, etc.)

This is mostly an unmodified prompt from Antrophic about how to build research agents.

### Language Engineering Agents (`lang-engineer`)

**Entrypoint agent:** `/language_architect_agent`

A comprehensive system for designing and implementing programming languages that compile to C, featuring specialized agents for each phase of language development:

- **Language Architect** - Overall language design coordination and requirements analysis
- **Language Analysis** - Requirements understanding and language paradigm selection
- **Lexer Engineer** - Tokenization and lexical analysis implementation
- **Parser Engineer** - Recursive descent parser construction
- **Compiler Engineer** - Code generation and optimization strategies
- **Runtime Engineer** - Memory management and execution runtime design
- **Memory Engineer** - Garbage collection and ownership system implementation
- **Object System Engineer** - Type system and object model design
- **Coroutine Engineer** - Async/await and stackless coroutine implementation
- **VM Engineer** - Virtual machine and bytecode execution systems

**Key features:**
- C-targeted compilation with readable output
- Modern memory management with Rust-like ownership semantics
- Built-in coroutine and async/await support
- Hand-written parsers following libuv-style patterns
- Minimal dependencies for maximum portability
- Complete toolchain from lexer to code generation
