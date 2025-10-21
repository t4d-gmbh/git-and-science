```{include} ../README.md
:end-before: <!-- include-before -->
```

{% if build == "slides" %}
:::{admonition} Authors
:class: note, margin
Dr. Jonas I. Liechti  
Dr. Matteo Delucchi
:::

:::{admonition} Editors
:class: note, margin
Barbara Mejia
:::
{% else %}
### Authors

**Dr. Jonas I. Liechti**  
**Dr. Matteo Delucchi**

### Editors

**Barbara Mejia**
{% endif %}


### Content
```{toctree}
:maxdepth: {% if build == "slides" %}1{% else %}4{% endif %}
{% if build == "slides" %}:numbered:{% endif %}

content/intro/index
content/project_mgmt_tools/index
content/lfs/index
content/submodules/index
content/versioning_vs_reproducibility/index
content/exercise/index
```
