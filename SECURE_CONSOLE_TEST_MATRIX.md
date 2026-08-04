# Secure Console test matrix

| Case | Expected |
|---|---|
| No stored session | Credential gate remains visible |
| Invalid credential | Access denied and credential not stored |
| Valid individual credential | Temporary session created and Console opens |
| Browser refresh in same tab | Stored session verifies and Console reopens |
| Browser/tab closed | Session storage is removed locally |
| Sign out | Server session revoked and local session cleared |
| Mobile-app checkout without permission | Gateway returns 403 |
| Mobile-app checkout with permission | Existing payment-link workflow succeeds |
| AI Receptionist actions | Continue through authenticated gateway |

Browser-to-Supabase execution remains required before replacing the default Console URL.
