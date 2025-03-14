<h1 align="center">Set Secret<br />
<div align="center">
  
  [![Build](https://github.com/action-pack/set-secret/actions/workflows/build.yml/badge.svg)](https://github.com/action-pack/set-secret/)
  [![Version](https://img.shields.io/github/v/tag/action-pack/set-secret?label=version&sort=semver&color=066da5)](https://github.com/marketplace/actions/set-secret)
  [![Size](https://img.shields.io/github/size/action-pack/set-secret/dist/index.js?branch=release/v1.08&label=size&color=066da5)](https://github.com/action-pack/set-secret/)
  
</div></h1>

Action to set a repository secret.

## Usage 🚀

```yaml
uses: action-pack/set-secret@v1
with:
  name: 'MY_SECRET'
  value: 'Lorem ipsun dolor simit'
  token: ${{ secrets.REPO_ACCESS_TOKEN }}
```

## Inputs 📝

### name

**Required** `String` Secret name.

### value

**Required** `String` Secret value to store.

### token

**Required** `String` Repository [Access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token)

### owner

**Optional** `String` Owners name.

### repository

**Optional** `String` Repository name.

### org

**Optional** `Boolean` Indicates the repo is an [organization](https://docs.github.com/en/github/setting-up-and-managing-organizations-and-teams/about-organizations).

### visibility

**Optional** `String` The visibility of the secret in organizations. Can be `all`, `private`, or `selected`, Defaults to `all`.

## FAQ 💬

  * ### Why do I get the error '*Resource not accessible by integration*'?

    This will happen if you use ```secrets.GITHUB_TOKEN```.

    You need to create a [personal access token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token) instead.

    Go to your Github settings, select 'Developer settings' --> 'Personal access tokens' --> 'Tokens (classic)' and create a new token. Store its value in a secret, for example ```MY_TOKEN```.

    Then refer to it like this:
    
    ```yaml
    token: ${{ secrets.MY_TOKEN }}
    ```

## Stars 🌟
[![Stars](https://starchart.cc/action-pack/set-secret.svg?variant=adaptive)](https://starchart.cc/action-pack/set-secret)
