# github-action-gitlab-ci-syntax-check
Validate the syntax of `.gitlab-ci.yml` files

[![Verify Action](https://github.com/simp/github-action-gitlab-ci-syntax-check/workflows/Verify%20Action/badge.svg)](https://github.com/simp/github-action-gitlab-ci-syntax-check/actions?query=workflow%3A%22Verify+Action%22)
[![tag badge](https://img.shields.io/github/v/tag/simp/github-action-gitlab-ci-syntax-check)](https://github.com/simp/github-action-gitlab-ci-syntax-check/tags)
[![license badge](https://img.shields.io/github/license/simp/github-action-gitlab-ci-syntax-check)](./LICENSE)


<!-- vim-markdown-toc GFM -->

* [Description](#description)
* [Usage](#usage)
* [Reference](#reference)
  * [Action Inputs](#action-inputs)
  * [Action Outputs](#action-outputs)
* [Contributing](#contributing)
* [Feedback & Questions](#feedback--questions)
* [License](#license)

<!-- vim-markdown-toc -->

## Description

A [Github action] to validate a `.gitlab-ci.yml` file against a GitLab
service's CI Linter API.

## Usage

```yaml
on: [push]
jobs:
  test_glci_syntax:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: simp/github-action-gitlab-ci-syntax-check@v1
```

## Reference

### Action Inputs

<table>
  <thead>
    <tr>
      <th>Input</th>
      <th>Required</th>
      <th>Description</th>
    </tr>
  </thead>

  <tr>
    <td><strong><code>gitlab_api_private_token</code></strong></td>
    <td>No</td>
    <td>GitLab API private token (might help with rate-limiting)</td>
  </tr>

  <tr>
    <td><strong><code>gitlab_api_url</code></strong></td>
    <td>No</td>
    <td>Specify a GitLab API other than gitlab.com<br /><em>Default:</em> <code>https://gitlab.com/api/v4</code></td>
  </tr>
</table>


### Action Outputs

<table>
  <thead>
    <tr>
      <th>Output</th>
      <th>Description</th>
    </tr>
  </thead>

  <tr>
    <td><strong><code>valid</code></strong></td>
    <td>Returns <code>"true"</code> if the <code>.gitlab-ci.yml</code> is valid</td>
  </tr>
</table>


## Contributing

This is an open source project open to anyone. This project welcomes
contributions and suggestions!

## Feedback & Questions

If you discover an issue, please report it on our Jira at
https://simp-project.atlassian.net/

## License

Apache 2.0, See [LICENSE](https://github.com/simp/github-action-gitlab-ci-syntax-check/blob/main/LICENSE) for more information.

[GitHub action]: https://github.com/features/actions
