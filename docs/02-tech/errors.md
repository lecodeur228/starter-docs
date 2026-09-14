# Errors

Stable technical codes (never translate these values). Clients switch on `code`.

| Code | HTTP | Meaning |
|------|------|---------|
| `VALIDATION_ERROR` | 422 | Invalid payload |
| `UNAUTHENTICATED` | 401 | Missing/invalid token |
| `FORBIDDEN` | 403 | Not allowed |
| `NOT_FOUND` | 404 | Missing resource |
| `INVALID_API_KEY` | 401 | Bad `X-API-KEY` |
| `ACCOUNT_INACTIVE` / `ACCOUNT_DISABLED` | 403 | User disabled |
| `OTP_INVALID` | 400 | Bad OTP |
| `OTP_EXPIRED` | 400 | OTP expired |
| `AUTH_METHOD_DISABLED` | 403 | Auth mode off |
| `PROFILE_INCOMPLETE` | 403 | Must complete profile |
| `SERVER_ERROR` | 500 | Unexpected |

TODO — add project-specific codes; keep backend + mobile + this table aligned.
