# Synthetic Open Schema

**Open, vendor-neutral specification for portable synthetic monitoring checks**

[![License](https://img.shields.io/badge/license-Apache%202.0-blue)](https://github.com/syntheticopenschema/spec/blob/main/LICENSE)
[![Version](https://img.shields.io/badge/version-v1.0.0-blue)](https://github.com/syntheticopenschema/spec/releases/tag/v1.0.0)
[![Status](https://img.shields.io/badge/status-stable-green)](https://github.com/syntheticopenschema/spec)

---

## What is Synthetic Open Schema?

Synthetic Open Schema (SOS) is an open specification that defines a vendor-neutral format for synthetic monitoring checks. Write your checks once, run them anywhere.

### 🎯 Key Features

✅ **Portable** — Define checks once, execute on any compatible runner
✅ **Vendor-Neutral** — Break free from platform lock-in
✅ **Declarative** — YAML-based, Kubernetes-style configuration
✅ **Production-Ready** — Stable v1.0.0 specification released
✅ **Open Source** — Apache 2.0 licensed, community-driven

---

## 🚀 Quick Example

```yaml
apiVersion: v1
kind: HttpCheck
metadata:
  name: api-health-check
spec:
  url: https://api.example.com/health
  interval: 1m
  checks:
    - type: statusCode
      value: 200
    - type: responseTime
      operator: lessThan
      value: 500ms
```

---

## 📦 Repositories

### Core

| Repository | Description | Status |
|------------|-------------|--------|
| [**spec**](https://github.com/syntheticopenschema/spec) | Normative specification (RFC-style docs) | ✅ v1.0.0 Stable |
| [**schemas**](https://github.com/syntheticopenschema/schemas) | JSON Schema definitions | ✅ Stable |

### Reference Implementations

| Repository | Description | Language | Status |
|------------|-------------|----------|--------|
| [**model**](https://github.com/syntheticopenschema/model) | Python Pydantic models | Python | ✅ Stable |
| [**runner**](https://github.com/syntheticopenschema/runner) | Python execution engine | Python | ✅ Stable |

---

## 🎓 Supported Check Types

### Core Checks (`apiVersion: v1`)

- **HttpCheck** — HTTP/HTTPS endpoint monitoring
- **TcpCheck** — TCP port connectivity
- **DnsCheck** — DNS resolution validation
- **TlsCheck** — TLS/SSL certificate monitoring
- **DomainCheck** — Domain registration checks

### Browser Checks (`apiVersion: browser/v1`)

- **LoadCheck** — Page load performance monitoring
- **ScriptedCheck** — Browser automation scripts

[View complete specification →](https://github.com/syntheticopenschema/spec)

---

## 🤝 Contributing

We welcome contributions from the community!

- 📝 **Spec Issues**: [syntheticopenschema/spec/issues](https://github.com/syntheticopenschema/spec/issues)
- 💬 **Discussions**: [syntheticopenschema/spec/discussions](https://github.com/syntheticopenschema/spec/discussions)
- 🔧 **Implementation**: Contribute to [model](https://github.com/syntheticopenschema/model) or [runner](https://github.com/syntheticopenschema/runner)
- 📚 **Documentation**: Help improve docs and examples

**Before contributing**, please read:
- [Contributing Guidelines](https://github.com/syntheticopenschema/spec/blob/main/CONTRIBUTING.md)
- [Code of Conduct](https://github.com/syntheticopenschema/spec/blob/main/CODE_OF_CONDUCT.md)
- [Governance](https://github.com/syntheticopenschema/spec/blob/main/GOVERNANCE.md)

---

## 🌟 Community Implementations

Building your own runner or client library? We'd love to feature it!

**Criteria for listing**:
- Implements the base Resource model
- Supports at least one check kind completely
- Documents which features are supported
- Clearly marks conformance level

[Open an issue](https://github.com/syntheticopenschema/spec/issues) to add your implementation!

---

## 📘 Resources

- 🌐 **Website**: [syntheticopenschema.org](https://syntheticopenschema.org) 
- 📖 **Specification**: [github.com/syntheticopenschema/spec](https://github.com/syntheticopenschema/spec)
- 🐍 **Python Package**: [PyPI - synthetic-open-schema-model](https://pypi.org/project/synthetic-open-schema-model/)
- 🏃 **Python Runner**: [PyPI - synthetic-open-schema-runner](https://pypi.org/project/synthetic-open-schema-runner/)
- 📊 **JSON Schemas**: [github.com/syntheticopenschema/schemas](https://github.com/syntheticopenschema/schemas)

---

## 🔐 Security

Found a security issue? Please review our [Security Policy](https://github.com/syntheticopenschema/spec/blob/main/SECURITY.md) for responsible disclosure.

**DO NOT** open public issues for security vulnerabilities. Instead:
- [Report privately via GitHub Security Advisory](https://github.com/syntheticopenschema/spec/security/advisories/new)

---

## 📜 License

All repositories in this organization are licensed under **Apache License 2.0** unless otherwise stated.

See individual repository LICENSE files for details.

---

## 🏛️ Governance

Synthetic Open Schema is stewarded by **Ideatives Inc.** and developed as an open specification.

- **Maintainer**: [@dmonroy](https://github.com/dmonroy)
- **Decision Process**: [Governance Model](https://github.com/syntheticopenschema/spec/blob/main/GOVERNANCE.md)
- **RFC Process**: New check types require 14-day community review

---

## 💡 Why Synthetic Open Schema?

### The Problem

Monitoring platforms use proprietary check formats, creating vendor lock-in. Migrating between platforms means rewriting all your checks.

### The Solution

Synthetic Open Schema provides a **common contract** — define your checks once in a standard format, run them on any compatible platform or runner.

### Benefits

- 🔄 **Portability**: Switch monitoring platforms without rewriting checks
- 🤝 **Interoperability**: Share check definitions across teams and tools
- 📊 **Consistency**: Same format for HTTP, DNS, TCP, TLS, browser checks
- 🚀 **Flexibility**: Build custom runners for your specific needs
- 🌍 **Open**: No vendor control, community-driven evolution

---

## 📣 Stay Connected

- 💬 [GitHub Discussions](https://github.com/syntheticopenschema/spec/discussions)
- 🐛 [Report Issues](https://github.com/syntheticopenschema/spec/issues)
- 🌟 [Star the Spec Repo](https://github.com/syntheticopenschema/spec)

