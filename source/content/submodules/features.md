## Features of <i class="fab fa-git"></i> Submodules
- **Separation**: {% if slide %}Submodules remain independent repositories, so their versioning history is separate from the parent repository.{% else %}Submodules remain independent repositories, so their versioning history is separate from the parent repository. This allows for better modularity and organization of code, as each submodule can evolve independently.{% endif %}
- **Pinning**: {% if slide %}Submodules are usually pinned to specific commits, ensuring reproducibility by locking them to a particular state.{%else%}Submodules are usually pinned to specific commits, ensuring reproducibility by locking them to a particular state. This means that when you clone the parent repository, you get the exact version of the submodule that was used at the time of the last commit.{% endif %}
- **Updates**: {% if slide %}Submodules can be updated independently or synchronized with the parent repository.{%else%}Submodules can be updated independently or synchronized with the parent repository. You can choose to pull the latest changes from the submodule's repository without affecting the parent repository, or you can update the submodule reference in the parent repository to point to a new commit.{% endif %}



