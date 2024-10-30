# Versioning ⚡️Reproducibility
{% if page %}
Git is an excellent tool for version control, tracking changes in code and allowing for collaborative development.
However, when it comes to **scientific reproducibility**, Git alone isn't sufficient.
Reproducibility requires more than just managing code—it also involves versioning data, tracking the environment, ensuring consistent execution, and documenting the workflow in a way that others can reliably reproduce the results.

{% else %}

### Git and Scientific Reproducibility

- **Git Strengths**:
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

./what_is_missing
./remote_services
./recap

```
{% else %}
<!-- BUILDING THE PAGES -->
```{include} ./what_is_missing.md
```
```{include} ./remote_services.md
```
```{include} ./recap.md
```
{% endif %}
