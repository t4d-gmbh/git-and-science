### GitHub Actions Example: Handling Submodules

In GitHub Actions, you can use the `actions/checkout` action with the `submodules` option set to `true` to ensure submodules are cloned and updated as part of the workflow.

**Example: GitHub Actions Workflow (`.github/workflows/ci.yml`)**

```yaml
name: CI with Submodules

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout repository with submodules
        uses: actions/checkout@v2
        with:
          submodules: true  # Initialize and update submodules
          fetch-depth: 0     # Ensure full history is fetched

      - name: Build Project
        run: |
          # Example build command
          make build
```

This ensures that the submodules are checked out and updated as part of your CI workflow.
