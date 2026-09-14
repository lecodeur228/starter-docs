# API

## Base URL

TODO — e.g. `https://api.example.com/api/v1`

## Conventions

- JSON only
- Standard envelope: `{ success, message, data, code?, errors? }`
- Clients branch on stable `code`, never on `message`
- Version prefix: `/api/v1`

## OpenAPI

TODO — link to Scramble / Scalar / exported OpenAPI from the backend

## Main resources

| Resource | Notes |
|----------|--------|
| Auth | see [authentication.md](authentication.md) |
| Users | TODO |
| Devices | TODO FCM tokens |
