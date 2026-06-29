# Antigrav Skills

This repository contains a collection of custom skills for the Antigravity AI coding assistant. These skills extend the assistant's capabilities and provide specialized domain knowledge and instructions for various areas of software development.

## Repository Structure

The core of this repository is the `skills` directory, which houses the individual skill modules.

### Available Skills

* **`devops_expert`**: Specialized knowledge for DevOps, CI/CD, Infrastructure as Code, Cloud Architecture (AWS/Azure/GCP), Docker, Kubernetes, and observability tasks.
* **`frontend_expert`**: Expertise in modern frontend web development, UI/UX design, and frameworks like Vue.js, Angular, Svelte, Solid.js, Astro, Tailwind CSS, and Web Components.
* **`golang_expert`**: Comprehensive instructions for Go (Golang) programming, including concurrency, web development, microservices, gRPC, testing, and building CLI applications.
* **`python_expert`**: Guidelines and best practices for Python programming, AI/ML, Data Science, FastAPI backends, script automation, and general Python development.
* **`serverless_expert`**: Domain knowledge for building serverless architectures, working with AWS Lambda, Azure Functions, Cloud Run, edge computing, serverless frameworks, and optimizing cloud costs.
* **`webdev_expert`**: Broad expertise covering general web development tasks, HTML, CSS, progressive web apps (PWAs), web performance, accessibility, web security, browser APIs, and web typography.

### Other Files

* **`AGENTS.md`**: Global or workspace-scoped rules for the agent, providing behavioral constraints and guidelines.
* **`mcp_config.json`**: Configuration for Model Context Protocol (MCP) servers, if applicable.

## How it Works

The Antigravity assistant automatically discovers and loads these skills. Each skill folder contains a `SKILL.md` file that defines its name, description, and detailed instructions. When the assistant encounters a task that aligns with a skill's description, it will read the `SKILL.md` file and adopt the specialized instructions provided within to better assist with the task.
