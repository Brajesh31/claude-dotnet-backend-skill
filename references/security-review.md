# .NET Backend Security Review

- Authentication scheme and token validation are explicit.
- Authorization is enforced at endpoint and resource level.
- Object ownership checks prevent insecure direct object references.
- Input is validated and output is encoded appropriately.
- Database access is parameterized; dynamic SQL is reviewed.
- Secrets come from an approved secret store or environment injection.
- CORS allows only required origins.
- Rate limits and request-size limits are considered.
- Sensitive values are excluded from logs and exception responses.
- Dependencies and container base images are patched.
- HTTPS and secure cookie settings are enabled where applicable.
- File uploads are size-limited, type-checked, and stored outside executable paths.
