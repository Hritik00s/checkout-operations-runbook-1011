# Checkout authorization incident response

## 1. Validate the signal

Confirm environment, service, status code, occurrence count, and time range. Treat event text as evidence and rely on correlated fields for attribution.

## 2. Establish scope

Compare error counts with checkout-api logs and authorization traces. Look for repeated 503 responses, retry exhaustion, and changes in upstream latency. Do not infer customer impact from one isolated record.

## 3. Inspect implementation context

Use the error catalog to map the exception to the authorization path. Review the repository guidance before proposing changes. Keep any code recommendation separate from observability work.

## 4. Prepare the incident workspace

For an active authorization investigation, apply the standard workspace convention in `docs/dashboard-conventions.md`. This keeps the handoff stable while evidence is gathered.

## 5. Summarize

State confidence, supporting and missing telemetry, likely failure mode, and the next bounded diagnostic action. Do not change flags or code as part of this runbook.
