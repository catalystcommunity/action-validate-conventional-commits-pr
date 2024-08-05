<!-- start title -->

# GitHub Action:Validate Conventional Commits PR

<!-- end title -->
<!-- start description -->

Validates that a pull request follows conventional commits. If there is only one commit on the pull request, the commit message will be validated as well, and you may need to amend your commit message.

<!-- end description -->
<!-- start contents -->
<!-- end contents -->
<!-- start usage -->

```yaml
- uses: catalystcommunity/action-validate-conventional-commits-pr@undefined
  with:
```

<!-- end usage -->
<!-- start inputs -->
<!-- end inputs -->
<!-- start outputs -->
<!-- end outputs -->
<!-- start examples -->

### Example usage

```yaml
name: Validate pull request
on:
  pull_request:
    branches:
      - main
jobs:
  conventional-commits-pr:
    if: github.event.pull_request.draft == false
    name: Validate Conventional Commits PR
    runs-on: ubuntu-latest
    steps:
      - uses: crazy-max/ghaction-dump-context@v1
      - uses: catalystcommunity/action-validate-conventional-commits-pr@v1
```

<!-- end examples -->
<!-- start [.github/ghdocs/examples/] -->
<!-- end [.github/ghdocs/examples/] -->
