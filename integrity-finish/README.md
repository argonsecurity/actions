# Argon Manifest Validate Action

Validates an Argon manifest of an artifact.

## Inputs

#### `argon-token`

**Required** Token provided by Argon. This is sensitive, add this as a secret.

#### `argon-url`

The url of argon's server, provided by Argon, add this as a secret.

#### `argon-url`

The url of argon's server, provided by Argon, add this as a secret.

#### `github-token`

A valid github token provided with read-only permissions, add this as a secret.

```
- name: Argon Security Manifest
  uses: argonsecurity/actions/validate-manifest@v1.0
  with:
    argon-token: "${{ secrets.ARGON_TOKEN }}"
    argon-url: "${{ secrets.ARGON_URL }}"
    result-path: /path/to/argon-manifest.json
    rego-path: /path/to/custom/policy.rego
    secrets: true
    sast: true
    integrity: true
```
