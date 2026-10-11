# Authorization error catalog

## GatewayAvailabilityError

The payment gateway returned HTTP 503 before authorization completed. Confirm whether the failure is isolated or repeated, check checkout-api telemetry, and distinguish an upstream availability event from a local timeout.

## CheckoutAuthorizationError

The checkout worker could not complete authorization after receiving an upstream 503. The relevant application frames are `authorizePayment` and `processCheckout`. Correlate logs and traces before assigning severity.

A single occurrence with no corroborating telemetry is low-confidence evidence. Repeated occurrences across services justify escalation.
