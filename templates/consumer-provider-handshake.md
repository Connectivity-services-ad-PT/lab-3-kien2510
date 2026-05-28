# Consumer-Provider Handshake - team-notify

## Provider
- **Service:** Notification Service
- **Team:** Nhóm 7A
- **Contract:** contracts/notify.openapi.yaml

## Consumer
- **Service:** AI Vision Service
- **Contract:** contracts/ai-vision.openapi.yaml
- **Mock URL:** http://localhost:4011

## Endpoints consumed
| Endpoint | Method | Purpose |
|---|---|---|
| /health | GET | Check AI Vision availability |
| /detect | POST | Trigger image detection |

## Handshake Agreement
- Consumer tested against AI Vision mock at port 4011
- Provider contract lint passed with 0 errors
- Consumer-side smoke tests pass on mock environment
- Known: AI Vision /detect returns 400 for minimal payload - acceptable on mock

## Sign-off
- Provider: Nguyễn Trung Kiên - team-notify
- Date: 2026-05-28
