## Benefits for Reproducibility

- **Pinning Submodules**: {% if slide %}By pinning submodules to specific commits, you ensure the same version of an external library, dataset (_remember <i class="fab fa-git"></i> LFS!_), or tool is always used, which is crucial for reproducibility in complex projects.{% else %} By pinning submodules to specific commits, you ensure the same version of an external library, dataset (_remember <i class="fab fa-git"></i> LFS!_), or tool is always used, which is crucial for reproducibility in complex projects.
  This helps avoid issues that arise from changes in dependencies.{% endif %}
- **Independent Versioning**: {% if slide %}Each submodule has its own versioning history, allowing it to be maintained separately from the parent project.{% else %}Each submodule has its own versioning history, allowing it to be maintained separately from the parent project.
  This means that updates or changes in a submodule do not directly impact the parent repository unless explicitly updated.{% endif %}
- **Flexibility**: {% if slide %}Submodules can be easily updated or switched to different versions without affecting the rest of the project.{% else %}Submodules can be easily updated or switched to different versions without affecting the rest of the project.
  This flexibility allows developers to experiment with new features or fixes in a submodule while keeping the main project stable.{% endif %}
