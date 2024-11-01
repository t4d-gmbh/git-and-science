# Versioning ⚡️Reproducibility
{% if page %}
<i class="fab fa-git"></i> is an excellent tool for version control, allowing you to track changes in code and facilitate collaborative development.
However, achieving **scientific reproducibility** requires more than just using <i class="fab fa-git"></i>.

Reproducibility encompasses not only code management but also the versioning od data, tracking the computational environment, ensuring consistent execution, and thoroughly documenting the workflow. This comprehensive approach enables others to reliably reproduce your results.

{% endif %}

{% if slide %}
<!-- BUILDING THE SLIDES -->
```{toctree}
:maxdepth: 1

./git_vs_sci_reproducibility
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
<!-- ```{include} ./git_vs_sci_reproducibility.md
``` -->
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
