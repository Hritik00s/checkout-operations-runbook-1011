# Checkout operations repository context

This repository is the operational source of truth for the checkout-api authorization path. For production HTTP 503 investigations, read `docs/error-catalog.md` and `docs/incident-response.md` before choosing remediation. Follow `docs/dashboard-conventions.md` for the incident workspace.

Keep remediation limited to observability. Do not change feature flags, application code, integrations, repositories, or access controls unless the operator explicitly asks for that separate work.
