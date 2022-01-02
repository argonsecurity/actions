# Argon Manifest Action

Generates an Argon manifest of an artifact

## Inputs

#### `argon-token`

**Required** Token provided by Argon. This is sensitive, add this as a secret

#### `github-token`

A valid github token provided with read-only permissions, add this as a secret.

#### `artifact-path`

The local path of the artifact or the image name and tag

#### `argon-url`

The url of argon's server, provided by Argon, add this as a secret.

## Example usage

```
- name: Argon Security Manifest
  uses: argonsecurity/manifest-action@v1.0
  with:
    github-token: "${{ secrets.GITHUB_TOKEN }}"
    argon-token: "${{ secrets.ARGON_TOKEN }}"
    argon-url: "${{ secrets.ARGON_URL }}"
    artifact-path: "image:tag"
```
