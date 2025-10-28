# <i class="fab fa-git"></i> Submodules <i class="fa-solid fa-folder-tree"></i>
{% if slide %}
<!-- BUILDING THE SLIDES -->

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
./exo_inspect_course_content

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
```{include} ./exo_inspect_course_content.md
```
{% endif %}

