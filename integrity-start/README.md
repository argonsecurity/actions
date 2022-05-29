# Argon Manifest Validate Action

Validates an Argon manifest of an artifact.

## Inputs

#### `argon-token`

**Required** Token provided by Argon. This is sensitive, add this as a secret.

#### `argon-url`

The url of argon's server, provided by Argon, add this as a secret.

## Example usage

```
- name: Argon Security Integrity Start
  uses: argonsecurity/actions/integrity-start@v1.0
  with:
    argon-token: "${{ secrets.ARGON_TOKEN }}"
    argon-url: "${{ secrets.ARGON_URL }}"
```
