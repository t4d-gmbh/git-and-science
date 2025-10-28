### <i class="fab fa-github"></i> GitHub Workflow Example
{% if page %}
In GitHub Actions {octicon}`play;0.8em`, you can use the `actions/checkout` action with the `submodules` option set to `true` to ensure submodules are cloned and updated as part of the workflow.
{% endif %}
**Example: GitHub {octicon}`play;0.8em` Workflow (`.github/workflows/ci.yml`)**

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
          submodules: true   # Initialize and update submodules
          fetch-depth: 0     # Ensure full history is fetched

      - name: Build Project
        run: |
          # Example build command
          make build
```
{% if page %}
This ensures that the submodules are checked out and updated as part of your CI workflow.
{% endif %}
