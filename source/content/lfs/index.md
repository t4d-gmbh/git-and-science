# <i class="fab fa-git"></i> Large File Storage (LFS) 
{% if slide %}
<!-- BUILDING THE SLIDES -->
```{toctree}
:maxdepth: 2

./why-use-git-lfs.md
./comparison-git-gitlfs.md
./git_data_model/index
./how-to-use-git-lfs.md
./gitLFS_UZH.md
```

{% else %}
<!-- BUILDING THE PAGES -->
<!-- build the page content here -->
```{include} ./why-use-git-lfs.md
```
```{include} ./comparison-git-gitlfs.md
```

# <i class="fab fa-git"></i> Data Model

Let's dive deeper into the technical details of how <i class="fab fa-git"></i> and <i class="fab fa-git"></i> LFS handle files.

```{include} ./git_data_model/git_data_model.md
```
```{include} ./git_data_model/gitLFS_data_model.md
```

```{include} ./how-to-use-git-lfs.md
```
```{include} ./gitLFS_UZH.md
```
{% endif %}
