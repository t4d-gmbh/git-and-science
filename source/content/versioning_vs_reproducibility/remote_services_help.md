## How Remote Services Can Enhance Reproducibility
{% if slide %}
:::{tip}
:class: margin
Checkout [git-and-its-remotes](https://t4d-gmbh.github.io/git-and-its-remotes) and [ci-cd-workflows](https://t4d-gmbh.github.io/ci-cd-workflows) to learn about the benefits of remote services like <i class="fab fa-github"></i> **GitHub** and <i class="fab fa-gitlab"></i> **GitLab**.
:::
- **Improved Accessibility**: 
  - Remote services enhance accessibility, allowing researchers to easily share their work with the scientific community.

- **Collaboration Tools**: 
  - Features like Issues and Merge/Pull Requests significantly improve documentation.
  - These tools are effective for formalizing [features and tracking their implementation](https://t4d-gmbh.github.io/git-and-its-remotes/content/project_management/index.html#feature-branch-approach-reloaded).

- **Automation**: 
  - Enables automated processes triggered by various events within a Repository or Project.
  - Continuous Deployment (CD) is crucial for reproducibility in scientific analyses.

- **Automation Scripts**: 
  - Can declare the environment in which the analysis runs and the corresponding data versions used.
  - Provide comprehensive documentation of analyses, including data, scripts, dependencies, and execution environments.

{% else %}

If you've explored [git-and-its-remotes](https://t4d-gmbh.github.io/git-and-its-remotes) and [ci-cd-workflows](https://t4d-gmbh.github.io/ci-cd-workflows), you may have gained insights into how remote services like <i class="fab fa-github"></i> **GitHub** and <i class="fab fa-gitlab"></i> **GitLab** can improve the reproducibility of scientific analyses.

One of the most significant contributions of these platforms is improved accessibility.
Researchers can easily share their work, making it more available to others in the scientific community.

Collaboration tools, such as Issues and Merge/Pull Requests, play a significant role in enhancing documentation for analyses.
These tools are particularly effective for formalizing [features and track their implementation](https://t4d-gmbh.github.io/git-and-its-remotes/content/project_management/index.html#feature-branch-approach-reloaded).

Automation is another important aspect of remote services, which allows for automated processes to be triggered by various events within a Repository or Project.
Continuous Deployment (CD) is especially relevant to the reproducibility of scientific analyses:

Automation scripts can do more than just deploy a website; they can specify which scripts to run and the corresponding versions of the data used. Since automation scripts define the conditions for their execution and are part of the repository, they can comprehensively document and declaratively specify an analysis, detailing everything from the data utilized to the analysis scripts, their dependencies, and the specific environment in which the scripts were executed.
{% endif %}
