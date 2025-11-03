# Polyglot

**Intelligent and reproducible project scaffolding.**

Polyglot is a next-generation command-line tool that creates fully reproducible development environments. Stop fighting with "works on my machine" problems and start building with confidence.

🌐 [polyglot.build](http://polyglot.build)

## What is Polyglot?

Polyglot goes beyond simple project templates. It manages your entire development stack – from toolchain installation to service orchestration – using a declarative manifest that guarantees the same setup on every machine.

```bash
polyglot new polyglot/rails-api \
  --ruby_version="3.3.0" \
  --database="postgresql" \
  --postgres_version="16"
```

**In seconds, you get:**
- ✅ Version-pinned language runtimes and CLI tools (via `mise`)
- ✅ Running Docker services with health checks
- ✅ Rendered project templates
- ✅ Concurrent task execution based on a dependency graph
- ✅ A project that works identically for every developer

## Core Features

### 🎯 Reproducibility by Default
Every tool, runtime, and dependency is precisely version-pinned. No more debugging environment differences across your team.

### 📋 Declarative Manifests
Define your entire setup in a clean `pack.yaml` file. No fragile shell scripts, just a clear dependency graph of tasks.

### ⚡ Concurrent Orchestration
Polyglot builds a DAG from your tasks and runs them in parallel whenever possible, dramatically reducing setup time.

### 🧩 Composable Blueprints
Create reusable "mixins" (like PostgreSQL setup) and import them into any pack. Build a DRY ecosystem of components.

### 🐳 Smart Service Management
Integrated Docker services with automatic health checks. Tasks that need a database only run after it's ready.

### 🎨 Powerful Templating
Render not just file contents, but file names and directory structures too. Support for conditional logic and user parameters.

## Key Repositories

### [polyglot](https://github.com/polyglot-build/polyglot)
The main CLI tool. This is what developers install and run to scaffold new projects.

### [pack-registry](https://github.com/polyglot-build/pack-registry)
A self-hosted service for discovering and serving versioned packs. Integrates with GitHub to automatically index new pack releases.

### [renderfs](https://github.com/polyglot-build/renderfs)
A flexible Go library for rendering project templates from any `fs.FS` source using Pongo2. Powers Polyglot's templating engine.

## The Pack Ecosystem

Packs are reusable blueprints for projects. The community can create and share packs for any language or framework:

- `polyglot/rails-api` - Ruby on Rails API with PostgreSQL
- `polyglot/nextjs-app` - Next.js with TypeScript and Tailwind
- `polyglot/golang-cli` - Go CLI tool with Cobra
- ...and many more to come!

Each pack includes everything needed: parameters, services, setup tasks, and templates.

## Project Status

Polyglot is under active development with a **beta release planned before the end of 2024**. We're building a tool that will transform how teams bootstrap and maintain projects.

Want to be notified when we launch? **⭐ Star the repo** and watch for updates!

## Philosophy

We believe project scaffolding should be:
- **Reproducible** – Same result on every machine, every time
- **Declarative** – Clear manifests over magic scripts
- **Concurrent** – Fast setup through parallel execution
- **Composable** – Reuse components across projects

## Roadmap

- **V1 (Current)**: Perfect the "Day 1" local development experience
- **V2**: Add `polyglot provision` and `polyglot deploy` for infrastructure
- **V3**: Launch Polyglot Cloud, a managed PaaS for zero-friction deployment

## Get Involved

- ⭐ **Star our repos** to show support and stay updated
- 🐛 **Report issues** to help us improve
- 💡 **Suggest packs** you'd like to see in the ecosystem
- 📖 **Read the docs** at [polyglot.build](http://polyglot.build)

## License

All projects are open source under the MIT license.

---

Built by developers who are tired of broken project setup.
