# Security policy

## Supported versions

The latest SDK release is supported. Older releases and untagged `main`
commits receive fixes only by upgrading.

## Report a vulnerability

Do not open a public issue, discussion, or pull request for a suspected
vulnerability.

Use
[GitHub private vulnerability reporting](https://github.com/directorhq/escape-director-device-sdk/security/advisories/new)
to report it privately. Include:

- The affected board, SDK version or commit, and core and library versions.
- Reproduction steps or a minimal sketch.
- Expected and observed impact.
- Whether Room Connector or the hosted service may also be affected.

If private reporting is unavailable, email
[support@escapedirector.com](mailto:support@escapedirector.com) with a request
for a secure reporting channel. Do not include Wi-Fi passwords, pairing
records, certificates, or customer data in ordinary email.

Allow maintainers reasonable time to investigate, release a fix, and publish
an advisory before public disclosure.

## Scope

Useful reports include ways to read or change a Device's credentials or
pairing data, bypass TLS or broker authentication, send commands a sketch did
not declare, or crash or lock up a board from the network.
