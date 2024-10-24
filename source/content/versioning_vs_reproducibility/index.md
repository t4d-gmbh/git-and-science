# Versioning ⚡️Reproducibility

Git is an excellent tool for version control, tracking changes in code and allowing for collaborative development.
However, when it comes to **scientific reproducibility**, Git alone isn't sufficient.
Reproducibility requires more than just managing code—it also involves versioning data, tracking the environment, ensuring consistent execution, and documenting the workflow in a way that others can reliably reproduce the results.

{% if slide %}
<!-- BUILDING THE SLIDES -->
```{toctree}
:maxdepth: 2

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
