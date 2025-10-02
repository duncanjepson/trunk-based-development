# Security Policy

## Supported versions
We maintain the following lines:
- Current mainline (`master`)
- LTS branches: `release/2.1`, `release/3.5` (see EoL dates in `/docs/support-matrix.md`)

## Reporting a vulnerability
Please email security reports to **security@yourdomain.tld** (do not open public issues).
Include steps to reproduce and affected versions. We will acknowledge within **2 business days**.

## Disclosure
We coordinate fixes privately via GitHub Security Advisories. Patched versions are tagged
(e.g., `vX.Y.Z`) and release notes list CVE/issue details.

## Key expectations
- No secrets in code. Secret scanning is enforced.
- Changes to `/src/**/Security/**`, auth, build/release files require CODEOWNERS approval.
