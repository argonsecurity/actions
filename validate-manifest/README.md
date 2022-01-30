# Argon Manifest Validate Action

Validates an Argon manifest of an artifact.

## Inputs

#### `argon-token`

**Required** Token provided by Argon. This is sensitive, add this as a secret.


#### `result-path`

**Required** The path to the manifest (billy generate result) path.

#### `argon-url`

The url of argon's server, provided by Argon, add this as a secret.

#### `rego-path`

A path to a custom rego file.

#### `branch-protection`

Should check if there is a branch protection on the branch that triggered the artifact build. Defaults to `false`.

#### `iac`

Should check if there was an IaC scanning during the artifact build. Defaults to `false`.

#### `integrity`

Should check if there was an integrity check during the artifact build. Defaults to `false`.

#### `mfa`

Should check if the user who triggered artifact build has MFA enabled. Defaults to `false`.

#### `minimum-reviewers`

Should check if the Pull Request that triggered the artifact build has at least 2 approvals. Defaults to `false`.

#### `pull-request`

Should check if the artifact build was triggered by a Pull Request. Defaults to `false`.

#### `sast`

Should check if there was a SAST scanning during the artifact build. Defaults to `false`.

#### `secrets`

Should check if there was a Secrets scanning during the artifact build. Defaults to `false`.

### Pay Attention

**Although the validations are optional, in order to use this action you must enable at least one validation.**

## Example usage

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
