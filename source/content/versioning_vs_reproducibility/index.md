# Versioning ⚡️Reproducibility
{% if page %}
<i class="fab fa-git"></i> is an excellent tool for version control, tracking changes in code and allowing for collaborative development.
However, when it comes to **scientific reproducibility**, <i class="fab fa-git"></i> alone isn't sufficient.
Reproducibility requires more than just managing code—it also involves versioning data, tracking the environment, ensuring consistent execution, and documenting the workflow in a way that others can reliably reproduce the results.

{% else %}

### Git and Scientific Reproducibility

- **<i class="fab fa-git"></i> Strengths**:
  - Version control
  - Tracking code changes
  - Collaborative development

- **Limitations for Reproducibility**: Requires more than code management
  - Needs data versioning
  - Environment tracking
  - Consistent execution
  - Comprehensive workflow documentation

{% endif %}

{% if slide %}
<!-- BUILDING THE SLIDES -->
```{toctree}
:maxdepth: 1

./reproducibility
./what_is_missing
./reproduce/index
./git_helps
./git_helps_more
./git_helps_even_more
./remote_services_help
./recap

```
{% else %}
<!-- BUILDING THE PAGES -->
```{include} ./reproducibility.md
```
```{include} ./what_is_missing.md
```
```{include} ./reproduce/index.md
```
```{include} ./reproduce/documentation.md
```
```{include} ./reproduce/data_availability.md
```
```{include} ./reproduce/workflow_doc.md
```
```{include} ./reproduce/config_settings.md
```
```{include} ./reproduce/dependencies.md
```
```{include} ./reproduce/transitive_dependencies.md
```
```{include} ./reproduce/exec_env.md
```
```{include} ./git_helps.md
```
```{include} ./git_helps_more.md
```
```{include} ./git_helps_even_more.md
```
```{include} ./remote_services_help.md
```
```{include} ./recap.md
```
{% endif %}
