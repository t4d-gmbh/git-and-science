# CI/CD for Reproducibility
{% if slide %}
<!-- BUILDING THE SLIDES -->
```{toctree}
:maxdepth: 2

./run_an_analysis
./using_docker

```
{% else %}
<!-- BUILDING THE PAGES -->
<!-- build the page content here -->
```{include} ./run_an_analysis.md
```
```{include} ./using_docker.md
```
{% endif %}
