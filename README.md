# lgcorzo/xxml

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![Dark Gravity](https://img.shields.io/badge/Autonomous%20Factory-Dark%20Gravity-blueviolet?style=flat-square)](https://github.com/lgcorzo/rust_CACD_autonomous_factory)

> [!NOTE]
> **UPSTREAM STATUS & SOVEREIGN FORK PURPOSE:**
> Following upstream repository archiving and licensing shifts across the MinIO ecosystem, this repository is **actively maintained and hardened** under **@lgcorzo** as an essential infrastructure component of the **[Dark Gravity Autonomous CA/CD Factory](https://github.com/lgcorzo/rust_CACD_autonomous_factory)** ([Architecture Knowledge Base](https://notebook.google.com/notebook/116d5f03-2fb0-4fa7-bd7c-1c9849920abc)). Continuous security auditing, zero-CVE verification, and hardware SIMD optimizations are independently maintained to guarantee supply-chain sovereignty and operational continuity.

---

## 🛡️ Dark Gravity Factory: Technological Sovereignty & Security Rationale

### 1. Architectural Role in Dark Gravity
In the **Dark Gravity Autonomous CA/CD Software Factory (V7.2 / V7.3)**, High-performance XML 1.0 parser with namespace support for processing AWS S3 XML response payloads with minimal memory allocation.

### 2. Supply-Chain Sovereignty & Independent Maintenance
- **Insulation from Upstream License Closures:** When upstream open-source projects close distributions or alter licensing terms, Dark Gravity enforces **semantic mirroring and sovereign forks** to guarantee total independence from commercial vendors.
- **Autonomous Security Verification & Zero-CVE Policy:** This repository is continuously audited for CVEs and vulnerabilities, maintaining a 100% clean secret scanning posture. Regressions and upstream bugs are resolved directly within the autonomous factory ecosystem.
- **Compliance & Provenance:** Ensures cryptographic integrity and auditable lineage in compliance with the **EU AI Act**, **SOC 2 Type II**, and **Hazitek / SPRI** regulatory frameworks.

---

# xxml

> NOTE: This package is a fork of 'encoding/xml' from https://github.com/golang/go.

Package xml implements a simple XML 1.0 parser that understands XML name spaces, 
along with extended support for control characters such as following

```
var controlCharactersMap = map[rune][]byte{
        '\x00': []byte("&#x0;"),
        '\x01': []byte("&#x1;"),
        '\x02': []byte("&#x2;"),
        '\x03': []byte("&#x3;"),
        '\x04': []byte("&#x4;"),
        '\x05': []byte("&#x5;"),
        '\x06': []byte("&#x6;"),
        '\x07': []byte("&#x7;"),
}
```

XML 1.0 spec does not allow these control characters. However this package intends 
to support these characters to satisfy MinIO's needs for AWS S3 compatiblity.
