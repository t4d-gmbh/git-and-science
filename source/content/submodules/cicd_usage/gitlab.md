### <i class="fab fa-gitlab"></i> Pipeline: Handling Submodules
{% if page %}
In GitLab CI, you can add the `GIT_SUBMODULE_STRATEGY` option to ensure submodules are fetched during the CI pipeline.
{% endif %}
**Example: GitLab {material-outlined}`account_tree` Pipeline (`.gitlab-ci.yml`)**

```yaml

variables:
  GIT_SUBMODULE_STRATEGY: recursive  # Or 'normal'
  GIT_SUBMODULE_FORCE_HTTPS: "true"  # Rewrite url to use HTTPS
  GIT_SUBMODULE_DEPTH: 0             # Fetch full history

stages:
  - build

build_project:
  stage: build
  script:
    - make build
```
{% if page %}
You only need to set the `GIT_SUBMODULE_STRATEGY` variable and the submodules will be fetched.
{% endif %}
