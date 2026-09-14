# Authentication

Document **only the modes enabled** for this project (backend `.env` flags).

## Enabled modes

| Mode | Enabled | Notes |
|------|---------|--------|
| Password (email) | TODO | `AUTH_PASSWORD` |
| OTP email | TODO | `AUTH_OTP_EMAIL` |
| OTP phone | TODO | `AUTH_OTP_PHONE` |
| Google Sign-In | TODO | `AUTH_GOOGLE` + `GOOGLE_CLIENT_ID` |

## Endpoints (fill from backend)

| Method | Path | Mode |
|--------|------|------|
| POST | `/api/v1/auth/register` | Password |
| POST | `/api/v1/auth/login` | Password |
| POST | `/api/v1/auth/otp/request` | OTP |
| POST | `/api/v1/auth/otp/verify` | OTP |
| PATCH | `/api/v1/auth/profile` | OTP incomplete profile |
| POST | `/api/v1/auth/google` | Google |
| POST | `/api/v1/auth/logout` | All |
| GET | `/api/v1/auth/me` | All |

## OTP notes

- Verify returns `has_account` / `hasAccount` and `profile_completed` / `profileCompleted`
- New OTP users stay incomplete until profile is completed
- Incomplete users are blocked on most protected routes (`PROFILE_INCOMPLETE`)

## Google notes

- Client sends Google ID token; API returns Bearer access token

## Tokens

- Header: `Authorization: Bearer {token}`
- TODO — expiration, logout-all, etc.
