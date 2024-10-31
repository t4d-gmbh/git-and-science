```{include} ../README.md
:end-before: <!-- include-before -->
```
```{toctree}
:maxdepth: {% if build == "slides" %}1{% else %}4{% endif %}
:caption: Git and Science
{% if build == "slides" %}:numbered:{% endif %}

content/intro/index
content/project_mgmt_tools/index
content/lfs/index
content/submodules/index
content/versioning_vs_reproducibility/index
content/exercise/index
```
