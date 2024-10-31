### GitLab CI Example: Handling Submodules
{% if page %}
In GitLab CI, you can add the `GIT_SUBMODULE_STRATEGY` option to ensure submodules are fetched during the CI pipeline.
{% endif %}
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
{% if page %}
This will ensure that all submodules are initialized and updated before running the `make build` command.
{% endif %}