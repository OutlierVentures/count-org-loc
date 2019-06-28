# Count lines of code for a GitHub organisation

## Install

1. `git clone https://github.com/benbalter/count-org-loc && cd count-org-loc`
2. `gem install bundler`
3. `script/bootstrap`

## Usage

```
script/count [ORGANISATION_NAME]
```

For a single repo (e.g. counting the Indy repos under Hyperledger):

```
./countsingle [GIT_CLONE_URL]
```

## Counting private repositories

To look at private repositories, you'll need to pass a [personal access token](https://github.com/settings/tokens/new) with `repo` scope as `GITHUB_TOKEN`. You can do this by adding `GITHUB_TOKEN=[TOKEN]` to a `.env` file in the repository's root.

If you are working with GitHub Enterprise and want to change your URL, simply add `GITHUB_ENTERPRISE_URL=https://<ghe-url>/api/v3` to the `.env` file


Sample `.env` File :

```bash
GITHUB_TOKEN="<token>"
GITHUB_ENTERPRISE_URL="https://my-ghe.local/api/v3"
```
