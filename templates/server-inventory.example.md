# Server Inventory Example

Do not commit a real server inventory. Copy this file to a private, ignored location and replace placeholders locally.

```markdown
# Server Inventory

## <server-alias>

- Purpose: <production | staging | development>
- Environment: <cloud/vendor/region>
- Host/IP: <host-or-ip>
- SSH Port: <port>
- Login User: <user>
- Deployment Path: <deploy-root>
- Service Name: <service-name>
- Log Location: <log-path>
- Credential Reference: <local-secure-storage-reference>
```

Never store plaintext passwords, API keys, private keys, tokens, or database URLs here.
