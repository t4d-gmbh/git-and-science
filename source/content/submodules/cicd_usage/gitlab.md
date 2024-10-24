### GitLab CI Example: Handling Submodules

In GitLab CI, you can add the `GIT_SUBMODULE_STRATEGY` option to ensure submodules are fetched during the CI pipeline.

**Example: GitLab CI/CD Pipeline (`.gitlab-ci.yml`)**

```yaml
stages:
  - build

build_project:
  stage: build
  script:
    - git submodule sync
    - git submodule update --init --recursive
    - make build
  variables:
    GIT_SUBMODULE_STRATEGY: recursive  # Initialize and update submodules
```

This will ensure that all submodules are initialized and updated before running the `make build` command.
