## ... and More!
{% if slide %}
- **Independent Development**: 
  - Combining scripts and datasets in a single repository may not be optimal, as they can evolve separately, particularly datasets that may be utilized in various studies.

- **Utilizing Git Submodules**: 
  - Leverage `git submodule` to effectively connect multiple repositories.

- **Version Tracking**: 
  - With <i class="fab fa-git"></i> submodules, you can clearly specify the version of the data used for each version of your analysis.
{% else %}
To effectively track both your analysis scripts and the analyzed data (using <i class="fab fa-git"></i> LFS), it's essential to establish a connection between these two repositories.
While it's possible to combine scripts and data into a single repository, this approach may not be ideal since both the dataset and the analysis scripts can evolve independently.
This is especially true for datasets, which may be utilized in various studies.

Fortunately, <i class="fab fa-git"></i> offers `git submodule`, a feature designed specifically for linking git modules.

By using <i class="fab fa-git"></i> submodules, you can seamlessly and clearly connect multiple repositories, allowing you to specify the exact version of the data used in each version of your analysis.
{% endif %}