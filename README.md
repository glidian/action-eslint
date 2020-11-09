# Glidian `action-eslint`

This repo contains an updated github action that runs eslint on pull request
files. It is based off of [eslint-action](https://github.com/tinovyatkin/action-eslint).
ga
If you need to update the action, create a PR off of this branch
[release/v.1.0.x](https://github.com/glidian/action-eslint/tree/release/v1.0.x).
Once the PR is merged, please update the action in [Glidian](https://github.com/ryromano/Glidian),
to use the new version of the action.

## To reference a new version of this action:

Update the [PR Workflow](https://github.com/ryromano/Glidian/blob/master/.github/workflows/pull-requests.yml)
to use the new version.

You can reference the new workflow in a number of ways:

```yaml
# using a commit sha
 - uses: glidian/action-eslint@8716584
        with:
          repo-token: ${{secrets.GITHUB_TOKEN}}
          check-name: eslint

# using a branch name
 - uses: glidian/action-eslint@release/v.1.0.x
        with:
          repo-token: ${{secrets.GITHUB_TOKEN}}
          check-name: eslint

# using a release version
 - uses: glidian/action-eslint@v.1.0.2
        with:
          repo-token: ${{secrets.GITHUB_TOKEN}}
          check-name: eslint
```
