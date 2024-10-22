# <i class="fab fa-git"></i> Submodules
{% if slide %}
<!-- BUILDING THE SLIDES -->

- A git submodule is a repository within another repository.
- It helps manage external repositories in your main project.
- Useful for including third-party libraries or separately maintained dependencies.

```{toctree}
:maxdepth: 2

./use-cases-submodules

```
{% else %}
<!-- BUILDING THE PAGES -->
<!-- build the page content here -->

A git submodule is a repository embedded inside another repository. 
It allows you to include and manage external repositories within your main project. 
This is particularly useful for incorporating third-party libraries or dependencies that are maintained separately.

```{include} ./use-cases-submodules.md
```
{% endif %}

