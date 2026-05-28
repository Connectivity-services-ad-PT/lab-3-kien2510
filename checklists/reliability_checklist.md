# Reliability Checklist - team-notify

## Contract
- [x] Contract lint pass (0 errors)
- [x] All operations have 2xx response
- [x] All operations have 4xx error response
- [x] Error responses use ProblemDetails schema
- [x] Query parameters defined with types

## Mock Server
- [x] Prism mock server starts from contract
- [x] Mock server responds on port 4010
- [x] AI Vision mock server responds on port 4011

## Test Coverage
- [x] Happy path / Functional tests
- [x] Auth tests (no token returns 401)
- [x] Negative tests (missing fields returns 400)
- [x] Boundary tests (limit=1, high severity)
- [x] Consumer-side smoke test (AI Vision mock)
- [x] Local-only non-functional test (response time)

## Newman
- [x] Collection runs on mock environment
- [x] No hardcoded baseUrl or authToken
- [x] newman-report.xml generated
- [x] newman-report.html generated

## Known Limitations
- Mock server does not validate JWT token (wrong token returns 201)
- Mock server returns mock data for any UUID (non-existent ID returns 200)
- Consumer-side smoke: AI Vision /detect returns 400 for test payload (expected behavior)
