# Security policy

## Handling secrets
- Never commit API keys, access tokens, passwords, signing keys, certificates, or production data.
- Keep local values in ignored `.env` files. Commit only a sanitized `.env.example` with placeholder values.
- Store deployment credentials in the hosting provider's encrypted secrets manager.
- Rotate any credential that may have been committed or exposed; deleting it from the latest commit is not sufficient.

## Isolation
- Keep each application and its dependencies in its own repository and deployment.
- Do not share writable storage, environment files, or credentials between projects.
- Grant each deployment only the permissions it needs.

## Reporting
Please report suspected vulnerabilities privately to the repository owner. Include reproduction steps and impact; do not publish sensitive data in an issue.
