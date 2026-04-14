# Contributing to Awesome AI Agent Runtimes

Thank you for your interest in contributing! This guide will help you add new platforms or improve existing entries.

## Adding a New Platform

1. **Choose the right category**:
   - Cloud Sandboxes & Code Execution
   - Browser Automation & Web Agents
   - Development Environments
   - Self-Hosted Solutions
   - Container & VM Platforms
   - Specialized Runtimes

2. **Use the template** (adapt based on platform type):

```markdown
### **[Platform Name](https://platform-url.com)**
- **Type**: [Firecracker microVM / Container / Browser automation / etc.]
- **Boot time**: [Actual measured time]
- **Key features**:
  - [Feature 1]
  - [Feature 2]
  - [Feature 3]
- **Pricing**: [Free tier / Pay-per-use / Subscription / Enterprise]
- **Best for**: [Primary use case]
```

3. **Update the comparison matrix**:
   - Add a row to the relevant comparison table
   - Use ✅ and ❌ for boolean features
   - Be factual and specific with metrics

4. **Maintain alphabetical order** within each category

## Quality Standards

### Required Information
- Official website/documentation URL
- Clear description of isolation mechanism
- Accurate boot/cold start times (if applicable)
- Pricing model (even if just "Open source")
- Primary use case

### Prohibited
- Marketing fluff or promotional language
- Unverified claims or benchmarks
- Affiliate links
- Dead or abandoned projects (unless historically significant)

## Comparison Matrix Guidelines

When adding to comparison matrices:

- **Boot Time**: Use realistic cold start times (not best-case marketing claims)
- **Isolation**: Specify the actual isolation technology (Firecracker, gVisor, Docker, etc.)
- **GPU**: List specific models if available (A100, H100, RTX 4090, etc.)
- **Pricing**: Be specific (per-second, per-request, subscription, free tier details)

## Example: Good vs. Bad Entries

### ❌ Bad
```markdown
### **AwesomeSandbox**
- The best sandbox platform ever!
- Super fast!
- Use our affiliate link: [sign up here]
```

### ✅ Good
```markdown
### **[AwesomeSandbox](https://awesomesandbox.io)**
- **Type**: Firecracker microVM
- **Boot time**: ~1-2 seconds (snapshot-based)
- **Key features**:
  - Python & Node.js support
  - 2 vCPU / 4 GB RAM per sandbox
  - File upload/download APIs
  - Auto-scaling
- **Pricing**: Free tier (100 hours/mo), then $0.02/hour
- **Best for**: AI code execution, data processing
```

## Submitting Changes

1. Fork the repository
2. Create a feature branch (`git checkout -b add-awesome-platform`)
3. Make your changes
4. Ensure markdown formatting is correct
5. Submit a pull request with a clear description

## Questions?

Open an issue for discussion before adding:
- Platforms you're affiliated with (disclosure required)
- Controversial or competing platforms
- Major reorganization of categories

Thank you for helping make this list better! 🚀
