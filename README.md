# action-sync-fork

Syncs galaxy integration forks with upstream

## Example Usage (workflow) - OUTDATED
[`.github/workflows/sync.yml`](https://github.com/GOG-Nebula/galaxy-riot-integration/blob/9da15bdfd5f30f2aa6e887491d7f53d0853adeae/.github/workflows/sync.yml)
```yaml
name: sync-upstream
on:
  schedule:
    - cron: '23 * * * *'
  workflow_dispatch:
jobs:
  sync:
    runs-on: ubuntu-latest
    steps:
      - uses: GOG-Nebula/syncer@feature/initial
        with:
          upstream_owner: urwrstkn8mare
          upstream_repo: galaxy-riot-integration
          upstream_branch: test
          reviewers: urwrstkn8mare,UncleGoogle,AndrewDWhite
          token: ${{ secrets.GITHUB_TOKEN }}
```

**_NOTE: should not be used in an integration (eg. cron value is just a random value)_**

## TODO

- [ ] better logging in the action
- [x] update the readme
- [x] fix this repo's workflows (incl making them use yarn instead of npm)
- [ ] add tests (maybe not worth it)
- [ ] improve code readablitiy
