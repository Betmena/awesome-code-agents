[![Releases](https://img.shields.io/badge/Releases-v1.0-blue?logo=github&logoColor=white)](https://github.com/Betmena/awesome-code-agents/releases)

# AI Code Agents for Developers: IDEs, Tools, and Workflows 2025

English | [中文](README.zh-CN.md)

<!-- Hero image -->
![AI Code Agents](https://images.unsplash.com/photo-1555066931-4365d14bab8c?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=0b490dfb48a3d1b9a99f5f6b2d8c9b1c)

Table of Contents
- About this list
- Quick start
- Releases
- How to read this list
- AI-Enhanced IDEs & Editors
- Agentic IDEs and Platforms
- Extensions, Plugins, and SDKs
- Agent frameworks and runtimes
- Typical agent workflows
- Core patterns and recipes
- Example configs and prompt templates
- Integrations and CI/CD
- Security and data handling
- Performance and cost tips
- Comparison matrix
- How to contribute
- Code of conduct
- License
- Credits and resources

About this list
This repository catalogs AI-powered code agents, IDEs, extensions, and tools that help developers write, test, refactor, and ship code with AI assistance. It groups items by role and function. Each entry includes a short description, key features, integration notes, and a short usage tip. Use this list to discover tools, compare options, and build agent-driven workflows.

Quick start
- Browse the AI-Enhanced IDEs section to find editors that add AI features to your coding flow.
- Check Agent frameworks for runtime and orchestration tools.
- Follow the example workflows to build a reproducible agent pipeline.
- Visit the release bundle for packaged content: https://github.com/Betmena/awesome-code-agents/releases. Download the listed file and execute it to install or run the packaged assets.

Releases
[![Releases](https://img.shields.io/badge/Releases-v1.0-blue?logo=github&logoColor=white)](https://github.com/Betmena/awesome-code-agents/releases)

The releases page contains packaged examples, reference agents, and sample configs. Download the release file from the link above and execute the installer or binary as described in the release notes. The release file contains runnable demos and sample pipelines that map to the examples in this README.

How to read this list
- Each entry includes a short description and a usage tip.
- Items include links to homepages or repos when available.
- Use the example workflows section to copy templates and configs.
- Add items with a PR. See the Contribute section for the process.

AI-Enhanced IDEs & Editors
This group lists editors and IDEs that integrate AI features into core developer experiences: code completion, refactor tools, testing, debugging, and multi-file edits driven by LLMs.

Cursor — Agentic editor with multi-file edits
- Website: https://cursor.com/
- Summary: A VS Code-style editor built for agentic editing. It expands the typical autocomplete by mapping higher-level intents to multi-file edits and refactors.
- Key features:
  - Context-aware code actions.
  - Agent sessions that maintain memory and context across the project.
  - Built-in terminal and replayable edit history.
- Integration tip:
  - Map agent actions to version control branches for safe review.
- Use case:
  - Large refactors that touch several modules in one command.

Windsurf — Cascade flow agents for code
- Website: https://windsurf.com/
- Summary: IDE that uses an agent flow model. Agents form chains of smaller tasks that together implement a complex change.
- Key features:
  - Cascade Flow: split tasks into planning, implementation, and validation agents.
  - Visual flow editor for agent pipelines.
  - Workspace-aware agents for project-level decisions.
- Integration tip:
  - Use the visual flow to prototype CI checks and test generation steps.

Kiro — Spec-driven agent IDE
- Website: https://kiro.dev/
- Summary: Experimental agentic IDE focused on spec-first development. Developers write specifications and the agent fills in code, tests, and build configs.
- Key features:
  - Spec-driven scaffolding.
  - Integration with AWS services for live testing.
  - Change tracking per spec.
- Integration tip:
  - Use for greenfield projects where spec-driven development reduces rework.

CodeBuddy — Multipurpose AI coding tools
- Website: https://www.codebuddy.com/
- Summary: A suite of coding assistants and editor extensions. Focus on automation of repetitive tasks and augmentation of developer knowledge.
- Key features:
  - Snippet and template generation.
  - Inline documentation and test generation.
  - Collaboration tools for pair-programming with AI.
- Integration tip:
  - Attach CodeBuddy to CI to generate tests on PRs.

Trae — ByteDance Builder Mode
- Website: https://www.trae.ai/
- Summary: AI IDE from ByteDance with a Builder Mode that can scaffold new projects from high-level prompts.
- Key features:
  - Project generation from requirements.
  - Built-in deployment templates.
  - Agent-based task automation for project maintenance.
- Integration tip:
  - Use Builder Mode to create a scaffold and then lock dependencies for reproducible builds.

Zed — High-performance Rust editor with AI
- Website: https://zed.dev/
- Summary: A fast editor built in Rust that integrates AI features while prioritizing low-latency editing.
- Key features:
  - 120fps editing performance.
  - Plugin API that supports LLM-based features.
  - Remote workspace support.
- Integration tip:
  - Use Zed for latency-sensitive sessions with live AI completions.

通义灵码 (Lingma) — Alibaba coding assistant
- Website: https://lingma.aliyun.com/
- Summary: An AI coding assistant from Alibaba Cloud. Offers IDE plugins and a standalone editor focused on Chinese language support and large enterprise workflows.
- Key features:
  - IDE plugins for mainstream editors.
  - Built-in corpora and private model support.
  - Enterprise-grade security and authentication.
- Integration tip:
  - Use private model mode for sensitive code bases.

Augment Code — Professional coding tools
- Website: https://www.augmentcode.com/
- Summary: A toolset focused on AI enhancements for code search and automated refactors.
- Key features:
  - Semantic code search driven by neural embeddings.
  - Multi-file refactor suggestions.
  - Integration with Git and code hosts.
- Integration tip:
  - Index your repo to enable fast semantic search over code history.

Agentic IDE features to look for
- Project-aware context: agents should read many files, not just the open buffer.
- Reproducible runs: support to replay agent runs, log actions, and attach diffs.
- Safe edits: create branches or patch files rather than editing main branch directly.
- Fine-grained permissions: limit agent access to certain files or services.

Agentic IDEs and Platforms
This section lists platforms that provide agent orchestration, developer-facing runtimes, or that wrap multiple AI capabilities into a developer product.

Agent platforms and highlights
- LangFlow-style visual editors: allow composition of LLM nodes into pipelines. Use them to build synthesize-validate-commit flows.
- Server-based orchestration: host agents in a service to centralize state, logs, and secrets.
- Workspace-level memory: store project facts and developer preferences to reduce context loss.

Example platforms
- Windsurf and Trae (already listed) provide both IDE and orchestration features.
- Kiro focuses on spec-driven development and integrates with cloud runtimes.
- Standalone orchestration frameworks (see Agent frameworks) complement these IDEs.

Extensions, Plugins, and SDKs
This group lists individual plugins and SDKs that add AI features inside existing editors.

VS Code and JetBrains plugins
- AI autocomplete plugins: replace or augment built-in completions with model-backed suggestions.
- Test generation plugins: auto-generate unit and integration tests from docstrings or code.
- Refactor tools: use LLMs to propose refactors and show diffs inline.

Notable plugins
- GitHub Copilot (VS Code, JetBrains): model-backed completion and code generation.
- Codeium: completions and code actions with a plugin architecture.
- Local LLM plugins: wrap an on-prem model for completions and privacy.

Plugin integration tips
- Pin plugin versions for team parity.
- Add CI checks to catch unintended changes from agent edits.
- Use per-repo configuration to tune the model behavior.

Agent frameworks and runtimes
This section covers frameworks that let you build, chain, and run agents. Use these when you need custom orchestration or multi-model flows.

Patterns
- Planner-Executor pattern: a planner agent creates a plan. The executor agent performs concrete edits or API calls.
- Verifier pattern: run tests or validators after each change to ensure correctness.
- Memory + retrieval: store structured facts and retrieve them to augment prompts.

Frameworks and tools
- LangChain: prompt chaining, agent wrappers, GUI integrations. Good for building multi-step flows.
- LlamaIndex (now GPT Index): data connectors and retrieval to provide context to models.
- Agentic SDKs: frameworks that include tools for code editing, repo access, and test runners.

Runtime considerations
- Containerized agents: run agents inside isolated containers and bind mounts to repo.
- Sidecar model servers: host models locally and connect via HTTP or gRPC.
- Resource scaling: plan for CPU/GPU needs for local models.

Typical agent workflows
Below are tested workflows that combine IDE features, agents, and CI. Each workflow includes roles, steps, and example commands or prompts.

Workflow: New feature from spec
Roles: spec author, planner agent, code generator agent, test generator agent, CI validator.
Steps:
1. Author writes a short spec file in the repo: SPEC.md with acceptance criteria.
2. Planner agent reads SPEC.md and creates a task list:
   - scaffold modules
   - add API interfaces
   - add unit tests
3. Generator agent implements code per task.
4. Test generator creates tests and integration stubs.
5. Verifier agent runs tests locally. If failures, agent creates a patch and retries.
6. Agent opens a PR with the changes and a detailed changelog.

Example planner prompt
- "Read SPEC.md. Output a JSON array of tasks. Each task: id, description, affected_files, estimated_time_min."

Workflow: Bug fix with trace
Roles: bug reporter, trace collector, repair agent, verifier.
Steps:
1. Reproduce the bug with a short script.
2. Trace collector saves logs and stack traces to /tmp/trace.json.
3. Repair agent receives trace.json and the test that reproduces the bug.
4. Agent proposes a patch and a one-line reason.
5. Verifier agent runs tests and reports results.

Workflow: Continuous refactor
Roles: repo owner, refactor agent, human reviewer.
Steps:
1. Agent runs periodic analysis for deprecated APIs or anti-patterns.
2. It creates branch per refactor and attaches a summary with diffs.
3. Human reviewer inspects and merges.

Core patterns and recipes
This section gives patterns you can reuse and adapt. Each pattern lists intent, flow, and sample prompt skeleton.

Pattern: Plan -> Act -> Verify
Intent: Break tasks into plan and verify cycles to reduce regressions.
Flow:
- Planner builds a granular task list.
- Executor applies changes for one task.
- Verifier runs tests and lint per task.
Prompt skeleton for planner:
- "You are a planning agent. Given repo context and a high-level request, produce a sequence of atomic tasks in JSON format with affected files and run commands."

Pattern: Retrieval-augmented edits
Intent: Use repo search to provide context to the model.
Flow:
- Retrieve top-k relevant code snippets using embeddings.
- Concatenate snippets with a short task prompt.
- Ask the model to propose edits referencing snippet indices.
Note: keep token budgets in mind.

Pattern: Incremental patching
Intent: Produce small, testable patches rather than one large diff.
Flow:
- Agent splits a large change into N patches.
- Apply and test each patch sequentially.
- Roll back on failure.

Example configs and prompt templates
Store these in .agent or .yaml files in your repo. Use them as starting templates.

Sample agent config (YAML)
```yaml
agent:
  name: repo-refactor-agent
  model: gpt-4o-code
  max_steps: 8
  pre_hooks:
    - git fetch
    - git checkout -b agent/refactor-{{ timestamp }}
  tools:
    - type: shell
      allowed_cmds:
        - pytest
        - npm test
  verification:
    tests: pytest -q
```

Patch CLI example
```bash
# Run the agent locally with a simple wrapper
agent-run --config .agents/refactor.yaml --task "Modernize async APIs"
```

Prompt templates
- Commit message generator:
  "Create a concise commit message for the following changes. Include a one-line summary and a bullet list of impacted components."
- Test generator:
  "Generate unit tests in pytest for this function. Cover edge cases for inputs: [], None, large lists."

Integrations and CI/CD
Integrate agent runs in your CI to make agent edits auditable and repeatable.

CI pattern: agent PR bot
- Add a pipeline job that runs the agent on a schedule or on label triggers.
- Job runs in a container with the model endpoint set via secrets.
- Agent job creates a draft PR with a human reviewer tag.

Example GitHub Actions snippet
```yaml
name: Agent Refactor
on:
  schedule:
    - cron: '0 2 * * 1' # weekly
jobs:
  run-agent:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Run agent
        run: |
          agent-run --config .agents/weekly-refactor.yaml
      - name: Push branch
        run: |
          git push origin HEAD:refs/heads/agent/weekly-refactor
```

Secrets and config
- Store model keys and endpoints in your secret store.
- Use fine-grained tokens for agent actions.
- Rotate credentials and audit agent activity via logs.

Security and data handling
Manage access and data flow when agents access code and services.

Access control
- Limit agent scopes to the minimal set of files.
- Use a service account per agent for traceability.
- Approve agent runs for protected branches using human gates.

Data handling
- Keep private data out of model prompts unless using private, on-prem models.
- Use retrieval systems that sanitize sensitive content.
- Log agent actions without exposing secrets.

Model choice and privacy
- Self-hosted LLMs reduce data egress risk.
- Hybrid deployments: host a small local model for short prompts, call a remote model for large generation tasks.

Performance and cost tips
Optimizing for speed, token usage, and cost matters, especially for large repos.

Context window management
- Use retrieval to reduce prompt size.
- Cache common context like API stubs.
- Trim long files and index them via embeddings.

Batching and async runs
- Batch validations to reduce round trips.
- Use async executor patterns for long-running tasks.

Compute strategies
- Use CPU-only models for light tasks.
- Reserve GPU for heavy code generation or local model hosting.

Comparison matrix
Below is a short feature matrix to help compare options at a glance.

Features to compare
- Project context awareness
- Local model support
- Multi-file edits
- Reproducible runs
- Visual pipeline builder
- CI integration

Sample matrix (text)
- Cursor: high project context, multi-file edits, visual flows via agent sessions.
- Windsurf: cascade flows, visual pipeline builder, CI hooks.
- Kiro: spec-first, AWS integration, reproducible change sets.
- Zed: low-latency editing, plugin API, good for live coding sessions.
- Lingma: enterprise features, private models, strong Chinese language support.

How to contribute
This repo follows the typical open-source workflow. Use PRs to add items, update links, and propose corrections.

Contribution steps
1. Fork the repo and clone locally.
2. Add your item to the correct section in the README.
3. Provide a short description, website or repo link, and one usage tip.
4. Open a PR with the changes.
5. Keep PRs small and focused.

PR checklist
- New entries must include a link.
- Add an integration tip or usage note.
- Use plain English and short sentences.
- Include a license link if the item is a repo.

Code of conduct
Follow a simple code of conduct for all contributors:
- Be respectful in comments and PRs.
- Keep discussions constructive.
- Use issue threads to discuss large changes.

License
This list uses the CC0 / public domain spirit for the curated content and links. If you add code snippets or configs, license them clearly. For packaged releases, attach a clear license file.

Credits and resources
Curated resources and background reading:
- LangChain docs for prompt chaining and agents.
- LlamaIndex for retrieval augmented systems.
- Official vendor docs for Cursor, Zed, Windsurf, Kiro, and Trae.

Images and visual assets
Use the official logos and screenshots from each project for documentation. The hero image above comes from Unsplash and serves as a visual anchor. For product logos, link to the vendor-provided assets and follow each project's brand guidelines.

Appendix: Common prompts and templates
Use these templates in your agent configs to standardize behavior.

Change summary prompt
- "Given these diffs, produce a short changelog item with impacted modules and a risk score 1-5."

Refactor acceptance prompt
- "Explain why this refactor improves the code. List metrics or tests that validate the change."

Automated PR body template
- Title: [agent] short description
- Body:
  - What changed
  - Why
  - Tests run
  - Backward compatibility notes
  - How to revert

Example: PR body
```
Title: [agent] rename user_id to account_id across services

What changed:
- Renamed column and variable names in auth and billing services.

Why:
- Align with new product schema.

Tests:
- Ran unit tests for auth and billing.
- Integration tests passed locally.

Revert:
- Revert branch: agent/revert-rename-account
```

Practical tips for teams
- Add a one-page agent playbook to your internal docs.
- Decide which branches agents can push to.
- Keep a changelog for agent-driven PRs to track behavior drift.

Troubleshooting checklist
- If agents produce incorrect edits, reduce step complexity and increase verification.
- If prompts exceed token limits, move supporting context to retrieval store.
- If tests fail after agent edits, run the failing tests locally and attach the run logs to the agent run.

Sample agent-run scenarios and debug commands
- Reproduce a failing agent run locally with:
```bash
git checkout agent/branch
pytest tests/test_failing.py -q
```
- Generate a debug trace and upload to a tracking system:
```bash
agent-run --config .agents/debug.yaml --task "reproduce-bug" --trace /tmp/agent-trace.json
```

Resource links
- Cursor: https://cursor.com/
- Windsurf: https://windsurf.com/
- Kiro: https://kiro.dev/
- Zed: https://zed.dev/
- CodeBuddy: https://www.codebuddy.com/
- Trae: https://www.trae.ai/
- 通义灵码: https://lingma.aliyun.com/
- Augment Code: https://www.augmentcode.com/

Changelog
- v1.0: Initial curated list with workflows, templates, and example configs.

Releases and packaged assets
Visit the releases page to download runnable examples and packaged agents. Download the release file from https://github.com/Betmena/awesome-code-agents/releases and execute it as directed in the release notes. The released bundle includes sample agent configs, a small demo repo, and a runner script that you can run locally to see the workflows in action.

Frequently used file names in releases
- demo-agent-bundle.tar.gz
- run-demo.sh or run-demo.bat
- sample-configs/*.yaml
- README_RELEASE.md

If you need to test the demo
- Extract the bundle.
- Inspect sample-configs.
- Execute the runner script that matches your OS.
- The release includes a readme with exact run steps.

Maintenance and roadmap
Planned items:
- Add a dedicated section for local LLM hosting and tuning.
- Expand the matrix with more vendors and open-source models.
- Add reproducible notebooks and demo videos.

Contact and feedback
Open issues for corrections, additions, or to request a new category. Use PRs for content changes.

Legal and licensing
When you add links or code, respect upstream licenses. The curated list links to third-party projects. Include license pointers for any contributed code samples.

Acknowledgments
This list draws on public documentation, vendor pages, and community contribution. Thanks to the open-source teams that publish their tools and APIs.

End of file.