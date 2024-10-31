# <i class="fab fa-git"></i> Submodules <i class="fa-solid fa-folder-tree"></i>
{% if slide %}
<!-- BUILDING THE SLIDES -->

- A [<i class="fab fa-git"></i> submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) <i class="fa-solid fa-folder-tree"></i> is a repository within another repository.
- It helps manage external repositories in your main project.
- Useful for including third-party libraries or separately maintained dependencies.

```{toctree}
:maxdepth: 1
:hidden:

./what_are_submodules
./features
./benefits
./use-cases-submodules
./howto.md
./working_with
./gotchas.md
./cicd_usage/index

```
{% else %}
<!-- BUILDING THE PAGES -->
<!-- build the page content here -->


```{include} ./what_are_submodules.md
```
```{include} ./features.md
```
```{include} ./benefits.md
```
```{include} ./use-cases-submodules.md
```
```{include} ./howto.md
```
```{include} ./working_with.md
```
```{include} ./gotchas.md
```
```{include} ./cicd_usage/index.md
```
```{include} ./cicd_usage/github.md
```
```{include} ./cicd_usage/gitlab.md
```
{% endif %}

