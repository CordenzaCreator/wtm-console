# Secure mobile-app checkout

`close-secure.html` now routes `capture-inperson-lead` through the authenticated `close-console-gateway` operation `mobile_app_checkout`.

The permanent individual credential is still exchanged once and discarded. Only the temporary session is used for the app checkout request.

## Required backend dependency

The backend must include:
- `mobile_app_checkout` in the gateway allowlist
- `send_app_checkout` in closer permissions

## Verification

- A promoter must receive permission denied.
- A closer, SDR, manager, or CEO with `send_app_checkout` can send the existing official mobile-app payment link.
- Existing package validation, Stripe price selection, and lead capture remain owned by `capture-inperson-lead`.
- `close.html` remains unchanged for rollback.
