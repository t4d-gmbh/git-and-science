```{include} ../README.md
:end-before: <!-- include-before -->
```
```{toctree}
:maxdepth: {% if build == "slides" %}1{% else %}4{% endif %}
:caption: Git in Science
{% if build == "slides" %}:numbered:{% endif %}

content/intro/index
content/versioning_vs_reproducibility/index
content/lfs/index
content/submodules/index
content/project_mgmt_tools/index
content/ci_cd_for_repro/index
content/exercise/index
```
