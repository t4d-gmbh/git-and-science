# <i class="fab fa-git"></i> Submodules
{% if slide %}
<!-- BUILDING THE SLIDES -->

- A git submodule is a repository within another repository.
- It helps manage external repositories in your main project.
- Useful for including third-party libraries or separately maintained dependencies.

```{toctree}
:maxdepth: 2

./what_are_submodules
./features
./workflow
./use-cases-submodules
./cicd_usage/index

```
{% else %}
<!-- BUILDING THE PAGES -->
<!-- build the page content here -->


```{include} ./what_are_submodules.md
```
```{include} ./features.md
```
```{include} ./workflow.md
```
```{include} ./use-cases-submodules.md
```
```{include} ./cicd_usage/index.md
```
```{include} ./cicd_usage/github.md
```
```{include} ./cicd_usage/gitlab.md
```
{% endif %}

