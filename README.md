# Awesome AI Agent Runtimes [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of runtime environments and sandboxing platforms for AI agents to execute code, browse the web, and interact with systems safely.

AI agents need isolated, secure environments to run code, access tools, and perform tasks. This list covers platforms that provide sandboxed execution environments specifically designed for AI agents, LLMs, and autonomous systems.

## Contents

- [Cloud Sandboxes & Code Execution](#cloud-sandboxes--code-execution)
- [Browser Automation & Web Agents](#browser-automation--web-agents)
- [Development Environments](#development-environments)
- [Self-Hosted Solutions](#self-hosted-solutions)
- [Container & VM Platforms](#container--vm-platforms)
- [Specialized Runtimes](#specialized-runtimes)
- [Comparison Matrix](#comparison-matrix)

---

## Cloud Sandboxes & Code Execution

Managed platforms for running untrusted code from AI agents in isolated environments.

### **[Sandflare](https://sandflare.io)** 
- **Type**: Firecracker microVM sandboxes
- **Boot time**: < 1 seconds (snapshot-based)
- **Templates**: base, code-interpreter, browser-agent, ai-agent
- **Key features**: 
  - Firecracker microVM isolation (kernel-level)
  - Playwright + Chromium pre-installed (browser-agent)
  - LangChain, CrewAI, all LLM SDKs pre-installed (ai-agent)
  - Data science stack (pandas, numpy, matplotlib)
  - Python & Node.js SDKs
  - File upload/download, streaming execution
- **Pricing**: Pay-per-use, free tier available
- **Best for**: AI agents, browser automation, data analysis, code execution

### **[E2B](https://e2b.dev)**
- **Type**: Firecracker microVM sandboxes
- **Boot time**: <1 seconds
- **Templates**: Code interpreter, base
- **Key features**:
  - Firecracker isolation
  - Python & JavaScript SDKs
  - File system operations
  - Custom templates via Docker
  - Streaming output
- **Pricing**: Free tier + pay-per-use
- **Best for**: Code interpreters, AI coding agents

### **[Modal](https://modal.com)**
- **Type**: Serverless containers with GPU support
- **Boot time**: Cold start < 1 seconds
- **Key features**:
  - GPU support (A100, H100)
  - Python-native API
  - Persistent volumes
  - Scheduled jobs & cron
  - Model inference endpoints
- **Pricing**: Pay-per-second compute + GPU
- **Best for**: ML model serving, GPU workloads, batch processing

### **[RunPod](https://runpod.io)**
- **Type**: GPU cloud with serverless functions
- **Boot time**: Variable (serverless or persistent)
- **Key features**:
  - High-performance GPUs (A100, H100, RTX)
  - Serverless GPU functions
  - Persistent pods
  - Docker-based deployments
  - Cost-effective GPU pricing
- **Pricing**: Competitive GPU pricing, pay-per-second
- **Best for**: GPU-intensive AI workloads, model training

### **[Replicate](https://replicate.com)**
- **Type**: Serverless model hosting
- **Boot time**: Model-dependent (often <2s)
- **Key features**:
  - Run ML models via API
  - Automatic scaling
  - Version control for models
  - Pay-per-prediction
- **Pricing**: Per-prediction pricing
- **Best for**: Running pre-trained models, AI model APIs

### **[Cerebrium](https://cerebrium.ai)**
- **Type**: Serverless GPU inference
- **Boot time**: ~2-5 seconds
- **Key features**:
  - Serverless GPU deployment
  - Auto-scaling
  - Python SDK
  - Custom model deployment
- **Pricing**: Pay-per-second GPU compute
- **Best for**: Model deployment, serverless ML

### **[Pyodide](https://pyodide.org)** (In-browser)
- **Type**: Python in WebAssembly (browser-based)
- **Boot time**: ~1-3 seconds (client-side)
- **Key features**:
  - Run Python in the browser
  - NumPy, Pandas, Matplotlib support
  - No backend needed
  - Completely client-side
- **Pricing**: Free (open source)
- **Best for**: Client-side Python execution, demos

---

## Browser Automation & Web Agents

Platforms specialized in headless browser control for AI web agents.

### **[Browserbase](https://browserbase.com)**
- **Type**: Managed headless browser infrastructure
- **Key features**:
  - Playwright & Puppeteer compatible
  - Session recording & debugging
  - Proxy support
  - Stealth mode (anti-detection)
  - Live browser sessions
- **Pricing**: Subscription-based
- **Best for**: Web scraping, browser automation at scale

### **[Browserless](https://browserless.io)**
- **Type**: Headless Chrome as a service
- **Key features**:
  - Puppeteer & Playwright API
  - PDF generation
  - Screenshots
  - Docker deployable
  - Anti-bot detection features
- **Pricing**: SaaS or self-hosted
- **Best for**: PDF generation, screenshots, web automation

### **[Apify](https://apify.com)**
- **Type**: Web scraping & automation platform
- **Key features**:
  - Pre-built scrapers (actors)
  - Playwright & Puppeteer support
  - Proxy management
  - Data storage & exports
  - Scheduler
- **Pricing**: Free tier + pay-per-use
- **Best for**: Web scraping, data extraction

### **[Bright Data](https://brightdata.com)** (formerly Luminati)
- **Type**: Web data platform with browser automation
- **Key features**:
  - Massive proxy network
  - Browser unlocking
  - CAPTCHA solving
  - Web scraper IDE
- **Pricing**: Enterprise-focused
- **Best for**: Large-scale web scraping, proxy services

---

## Development Environments

Full-featured development environments for AI agents.

### **[Daytona](https://daytona.io)**
- **Type**: Standardized development environments
- **Key features**:
  - One-command workspace setup
  - Git provider integrations
  - Remote & local dev environments
  - Team collaboration
  - VS Code integration
- **Pricing**: Free (open source)
- **Best for**: Development workflows, team environments

### **[GitHub Codespaces](https://github.com/codespaces)**
- **Type**: Cloud-hosted VS Code environments
- **Boot time**: ~30-60 seconds
- **Key features**:
  - Full VS Code in browser
  - Pre-configured dev containers
  - GitHub integration
  - Persistent storage
- **Pricing**: Free hours/month, then pay-per-hour
- **Best for**: Development, code review

### **[Gitpod](https://gitpod.io)**
- **Type**: Automated cloud development environments
- **Boot time**: ~20-40 seconds
- **Key features**:
  - Ephemeral workspaces
  - VS Code, IntelliJ, or browser IDE
  - Git integration
  - Pre-builds for faster starts
- **Pricing**: Free tier + pay-per-hour
- **Best for**: Development, CI/CD integration

### **[Replit](https://replit.com)**
- **Type**: Collaborative browser IDE
- **Boot time**: Instant (browser-based)
- **Key features**:
  - 50+ languages
  - Real-time collaboration
  - Hosting included
  - AI code assistant
  - Package management
- **Pricing**: Free tier + paid plans
- **Best for**: Prototyping, education, collaboration

### **[CodeSandbox](https://codesandbox.io)**
- **Type**: Browser-based IDE for web development
- **Boot time**: Instant
- **Key features**:
  - React, Vue, Angular templates
  - npm package support
  - Live preview
  - Team collaboration
- **Pricing**: Free tier + paid plans
- **Best for**: Frontend development, prototyping

---

## Self-Hosted Solutions

Open-source platforms you can deploy on your own infrastructure.

### **[Firecracker](https://firecracker-microvm.github.io)**
- **Type**: MicroVM virtualization (AWS Lambda foundation)
- **Boot time**: ~125ms
- **Key features**:
  - Minimal overhead virtualization
  - Strong isolation (KVM-based)
  - Fast boot times
  - Small footprint
- **Pricing**: Free (open source)
- **Best for**: Building custom sandbox platforms

### **[gVisor](https://gvisor.dev)**
- **Type**: Application kernel for containers (Google)
- **Key features**:
  - OCI-compatible sandbox
  - Stronger isolation than Docker
  - Syscall interception
  - Compatible with Docker & Kubernetes
- **Pricing**: Free (open source)
- **Best for**: Secure container runtime

### **[Kata Containers](https://katacontainers.io)**
- **Type**: Lightweight VMs as containers
- **Key features**:
  - VM-level isolation with container UX
  - OCI-compatible
  - Kubernetes integration
  - Hardware-enforced isolation
- **Pricing**: Free (open source)
- **Best for**: Secure multi-tenant environments

### **[Docker](https://docker.com)** + **[Sysbox](https://github.com/nestybox/sysbox)**
- **Type**: Enhanced Docker runtime
- **Key features**:
  - Run systemd in containers
  - Nested container support
  - Improved isolation
  - Compatible with existing Docker workflows
- **Pricing**: Free (Docker CE + Sysbox open source)
- **Best for**: Running complex workloads in containers

### **[Podman](https://podman.io)**
- **Type**: Daemonless container engine
- **Key features**:
  - Rootless containers
  - Docker-compatible CLI
  - Kubernetes YAML support
  - Pod support
- **Pricing**: Free (open source)
- **Best for**: Secure container execution without daemon

---

## Container & VM Platforms

General-purpose platforms suitable for AI agent workloads.

### **[Fly.io](https://fly.io)**
- **Type**: Edge compute platform
- **Boot time**: ~1-3 seconds
- **Key features**:
  - Global edge deployment
  - Firecracker-based VMs
  - Persistent volumes
  - Anycast networking
  - Free tier (3 shared VMs)
- **Pricing**: Free tier + pay-per-use
- **Best for**: Low-latency global apps, edge computing

### **[Railway](https://railway.app)**
- **Type**: Simplified cloud platform
- **Boot time**: ~5-15 seconds
- **Key features**:
  - Git-based deployments
  - Database provisioning
  - Auto-scaling
  - Template marketplace
- **Pricing**: Free trial + pay-per-use
- **Best for**: Quick deployments, full-stack apps

### **[Render](https://render.com)**
- **Type**: Unified cloud platform
- **Boot time**: ~10-30 seconds
- **Key features**:
  - Automatic deploys from Git
  - Managed databases
  - Static sites & web services
  - Background workers
- **Pricing**: Free tier + subscription plans
- **Best for**: Web services, APIs, databases

### **[Google Cloud Run](https://cloud.google.com/run)**
- **Type**: Serverless containers
- **Boot time**: Cold start ~2-5 seconds
- **Key features**:
  - Auto-scaling from 0
  - Custom containers
  - Generous free tier
  - gVisor isolation
- **Pricing**: Free tier + pay-per-request
- **Best for**: Containerized APIs, microservices

### **[AWS Lambda](https://aws.amazon.com/lambda)**
- **Type**: Serverless functions (Firecracker-based)
- **Boot time**: Cold start ~1-10 seconds
- **Key features**:
  - Event-driven execution
  - Massive scale
  - Container image support
  - Extensive AWS integrations
- **Pricing**: Free tier + pay-per-invocation
- **Best for**: Event-driven workloads, AWS ecosystem

---

## Specialized Runtimes

Platforms with unique capabilities for specific AI agent use cases.

### **[Val Town](https://val.town)**
- **Type**: Social coding runtime
- **Boot time**: Instant (serverless)
- **Key features**:
  - TypeScript/JavaScript runtime
  - Instant API endpoints
  - Scheduled functions (cron)
  - Email, HTTP, webhooks
  - Public/private vals (functions)
- **Pricing**: Free tier + paid plans
- **Best for**: Quick scripts, webhooks, automation

### **[Pipedream](https://pipedream.com)**
- **Type**: Serverless integration platform
- **Boot time**: Instant
- **Key features**:
  - Pre-built integrations (1000+ apps)
  - Event-driven workflows
  - Node.js, Python, Go, Bash
  - Free tier with generous limits
- **Pricing**: Free tier + pay-per-invocation
- **Best for**: API integrations, workflow automation

### **[Deno Deploy](https://deno.com/deploy)**
- **Type**: Edge JavaScript/TypeScript runtime
- **Boot time**: < 1 second
- **Key features**:
  - Global edge deployment (35+ regions)
  - Zero-config deployments
  - Built-in KV store
  - Web standard APIs
- **Pricing**: Free tier + pay-per-request
- **Best for**: Edge functions, global APIs

### **[Cloudflare Workers](https://workers.cloudflare.com)**
- **Type**: Serverless V8 isolates
- **Boot time**: < 1ms (warm)
- **Key features**:
  - 300+ global locations
  - Zero cold starts
  - Workers AI (run ML models)
  - R2 storage, KV, D1 database
- **Pricing**: Free tier + pay-per-request
- **Best for**: Edge compute, global APIs, ultra-low latency

### **[Temporal](https://temporal.io)**
- **Type**: Workflow orchestration engine
- **Key features**:
  - Durable execution
  - Long-running workflows
  - State management
  - Retry & error handling
  - Event-driven architecture
- **Pricing**: Free (open source), managed cloud available
- **Best for**: Complex multi-step agent workflows

---

## Comparison Matrix

### Code Execution Platforms

| Platform | Isolation | Boot Time | GPU | Browser | Pre-installed Packages | Pricing Model |
|----------|-----------|-----------|-----|---------|----------------------|---------------|
| **Sandflare** | Firecracker microVM | <1s | ❌ | ✅ Playwright + Chromium | pandas, numpy, LangChain, CrewAI | Pay-per-use |
| **E2B** | Firecracker microVM | <1s | ❌ | ✅ Playwright | Custom via Docker | Free tier + usage |
| **Modal** | Container (gVisor) | <1s cold | ✅ A100, H100 | ❌ | pip install on demand | Per-second + GPU |
| **RunPod** | Docker/VM | Variable | ✅ RTX, A100, H100 | ❌ | Custom images | Per-second GPU |
| **Replicate** | Container | Model-dependent | ✅ | ❌ | Model-specific | Per-prediction |
| **Cerebrium** | Container | <1s | ✅ | ❌ | Custom Python env | Per-second GPU |
| **Pyodide** | WASM (browser) | 1-3s client-side | ❌ | N/A (runs in browser) | NumPy, Pandas, Matplotlib | Free (OSS) |

### Browser Automation Platforms

| Platform | Browser Engine | Proxy Support | Stealth Mode | Session Recording | Pricing |
|----------|---------------|---------------|--------------|-------------------|---------|
| **Sandflare (browser-agent)** | Chromium via Playwright | ❌ | Basic | ❌ | Pay-per-use |
| **Browserbase** | Chrome/Chromium | ✅ | ✅ Advanced | ✅ | Subscription |
| **Browserless** | Chrome | ✅ | ✅ | ✅ | SaaS or self-hosted |
| **Apify** | Chromium/Firefox | ✅ Extensive | ✅ | ✅ | Free tier + usage |
| **Bright Data** | Chrome | ✅ Massive network | ✅ Enterprise | ✅ | Enterprise |

### Development Environments

| Platform | Type | Boot Time | Persistence | IDE | Team Collab |
|----------|------|-----------|-------------|-----|-------------|
| **Daytona** | Dev containers | ~30-60s | ✅ | VS Code, JetBrains | ✅ |
| **GitHub Codespaces** | Cloud VM + VS Code | 30-60s | ✅ | VS Code (browser/desktop) | ✅ |
| **Gitpod** | Ephemeral workspaces | 20-40s | ✅ Optional | VS Code, IntelliJ | ✅ |
| **Replit** | Browser IDE | Instant | ✅ | Custom web IDE | ✅ Real-time |
| **CodeSandbox** | Browser IDE | Instant | ✅ | Custom web IDE | ✅ |

### Cloud Platforms (General Purpose)

| Platform | Type | Boot Time | Free Tier | Auto-scaling | Best For |
|----------|------|-----------|-----------|--------------|----------|
| **Fly.io** | Firecracker microVM | 1-3s | ✅ 3 VMs | ✅ | Global edge apps |
| **Railway** | Container | 5-15s | ✅ Trial credits | ✅ | Quick deployments |
| **Render** | Container | 10-30s | ✅ | ✅ | Web services |
| **Google Cloud Run** | Container (gVisor) | 2-5s cold | ✅ Generous | ✅ From 0 | Serverless containers |
| **AWS Lambda** | Firecracker | 1-10s cold | ✅ 1M requests/mo | ✅ | Event-driven |

### Edge / Serverless Runtimes

| Platform | Runtime | Global Locations | Cold Start | Max Duration | Best For |
|----------|---------|------------------|------------|--------------|----------|
| **Cloudflare Workers** | V8 isolate | 300+ | <1ms | 30s (free), unlimited (paid) | Ultra-low latency |
| **Deno Deploy** | V8 isolate | 35+ | <1s | No limit | TypeScript edge functions |
| **Val Town** | Node.js | US-based | Instant | 30s | Quick scripts, webhooks |
| **Pipedream** | Node.js/Python | US/EU | Instant | 5 min (free), 12h (paid) | API integrations |

### Self-Hosted Solutions

| Platform | Type | Complexity | Hardware Req | Maintenance | License |
|----------|------|------------|--------------|-------------|---------|
| **Firecracker** | MicroVM | High | KVM support | Manual | Apache 2.0 |
| **gVisor** | Container runtime | Medium | x86_64/ARM64 | Low | Apache 2.0 |
| **Kata Containers** | Lightweight VMs | Medium | Virtualization support | Medium | Apache 2.0 |
| **Docker + Sysbox** | Enhanced containers | Low | Standard Linux | Low | Apache 2.0 |
| **Podman** | Rootless containers | Low | Standard Linux | Low | Apache 2.0 |

---

## Selection Guide

### For AI Code Execution Agents
- **Best overall**: Sandflare (ai-agent template), E2B
- **With GPU needs**: Modal, RunPod, Cerebrium
- **Client-side**: Pyodide

### For Web Scraping / Browser Agents
- **Managed solution**: Sandflare (browser-agent), Browserbase
- **DIY**: Browserless (self-hosted), Apify

### For Multi-Agent Orchestration
- **Workflow engine**: Temporal
- **Serverless**: Pipedream, Cloudflare Workers
- **Long-running**: Fly.io, Railway

### For Development & Testing
- **Cloud IDE**: GitHub Codespaces, Gitpod, Replit
- **Standardized envs**: Daytona

### For Self-Hosted / On-Prem
- **Micro-VMs**: Firecracker (DIY), Kata Containers
- **Containers**: Docker + Sysbox, Podman, gVisor

### For Edge / Low-Latency
- **JavaScript/TS**: Cloudflare Workers, Deno Deploy
- **Global VMs**: Fly.io
- **API integrations**: Pipedream

---

## Key Considerations

When choosing an AI agent runtime, consider:

1. **Isolation Level**
   - Containers (Docker): Process isolation
   - gVisor/Kata: Enhanced container security
   - Firecracker: Hardware-level VM isolation

2. **Boot Time**
   - Critical for synchronous agent workflows
   - Snapshot-based systems (Firecracker) boot fastest
   - V8 isolates (Cloudflare Workers) have near-zero cold starts

3. **Pre-installed Dependencies**
   - Template systems (Sandflare, E2B) = no install overhead
   - Custom Docker images = flexibility but slower boots
   - Serverless = limited to runtime packages

4. **Resource Limits**
   - CPU/RAM per sandbox
   - Execution timeouts (seconds to hours)
   - Concurrent sandbox limits

5. **Pricing Model**
   - Per-second compute (most platforms)
   - Per-request (serverless)
   - Per-prediction (ML platforms)
   - Subscription (development platforms)

6. **SDK Quality**
   - Python & Node.js are most common
   - REST API fallback for other languages
   - Streaming support for long-running tasks

---

## Note:

All the data is fetched using AI agents and may not be 100% accurate. Please verify details from official sources before making decisions.

## Contributing

Contributions welcome! Please read the [contribution guidelines](CONTRIBUTING.md) first.

- Add new platforms with clear categorization
- Include key metrics (boot time, isolation type, pricing model)
- Update comparison matrix
- Maintain alphabetical order within categories

---

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0)

To the extent possible under law, the contributors have waived all copyright and related rights to this work.
