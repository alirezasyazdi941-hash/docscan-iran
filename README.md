# DocScan Iran

## Repository status

This repository has its security baseline and CI workflow configured. The original application source has not yet been imported, so this repository is **not yet an installable iPhone app**.

## iPhone installation target

The intended delivery format is a Progressive Web App (PWA), installable from Safari on iOS after it is deployed over HTTPS. The application source must provide:
- a valid web app manifest with an app name, icons, `start_url`, `scope`, and standalone display mode;
- an application entry point and responsive iPhone layout;
- service-worker/offline behavior where appropriate;
- no embedded API secrets or private credentials.

When source code is added, verify the app on a real iPhone using Safari → Share → Add to Home Screen. A native iOS app distributed through TestFlight/App Store is a separate signing and distribution process.

## Security and isolation

- This project is maintained in its own repository and should have its own deployment and environment variables.
- Keep secrets in the deployment platform's encrypted secret store; never commit them.
- Do not share writable storage or credentials with the other projects.
- Review permissions and third-party dependencies before deployment.

See [SECURITY.md](../SECURITY.md) for the repository security policy.
