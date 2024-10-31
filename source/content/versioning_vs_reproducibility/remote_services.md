### How Remote Services like GitHub or GitLab Bridge the Gap

:::{card} 1. **Data Versioning with Git LFS**
{% if page %}
**Git Large File Storage (Git LFS)** allows you to version large files that would otherwise slow down Git. Git LFS stores large files (such as datasets, images, or models) in a remote storage service but keeps a reference in the Git repository. This ensures that large datasets are versioned and can be retrieved by collaborators.

**Example: Using Git LFS for Data Versioning**

```bash
# Install Git LFS
git lfs install

# Track a large file with Git LFS
git lfs track "data/large_dataset.csv"

# Add, commit, and push as usual
git add data/large_dataset.csv
git commit -m "Add dataset"
git push
```

This enables version control for large datasets, making it easier for others to reproduce experiments with the exact same data.

{% else %}
The **Git LFS** extension allows to version large files. 
{% endif %}
:::
:::{card} 2. **Tracking Environments with GitLab CI/CD or GitHub Actions**
{% if page %}
Both **GitLab CI/CD** and **GitHub Actions** allow you to automate the setup of the software environment. By specifying dependencies and tools in these files, you ensure that the same environment is recreated every time the workflow is run, which is critical for reproducibility.

**Example: Environment Setup in GitHub Actions**

```yaml
name: Set up Python environment

on: [push]

jobs:
  setup-environment:
    runs-on: ubuntu-latest
    steps:
      - name: Check out code
        uses: actions/checkout@v2
      - name: Set up Python
        uses: actions/setup-python@v2
        with:
          python-version: '3.8'
      - name: Install dependencies
        run: pip install -r requirements.txt
```
{% else %}
Automated software env.-setup ensures that the same env is recreated every time the workflow is run.
{% endif %}
:::

:::{card} 3. **Combining Repositories with Git Submodules**
{% if page %}
Git **submodules** allow you to combine multiple repositories, such as a data repository (versioned with Git LFS) and a code repository. This helps manage large projects with distinct parts—such as data and analysis code—while keeping them in sync for reproducibility.

**Example: Adding a Data Repository as a Submodule**

```bash
# Add a data repository as a submodule
git submodule add https://github.com/username/data-repo.git data

# Clone the repository with its submodules
git clone --recursive https://github.com/username/analysis-repo.git
```
{% else %}
Git **submodules** combine multiple repositories, such as a data and a code repo.
{% endif %}
:::

:::{card} 4. **Workflows and Automation with CI/CD**
{% if page %}
By using GitHub Actions or GitLab CI/CD, you can automate workflows that run your analysis every time new code or data is pushed. This automates the execution of your work, ensuring that changes are tested and results are regenerated consistently, making the process reproducible end-to-end.

**Example: Automating Analysis with GitLab CI**

```yaml
stages:
  - data_preprocessing
  - analysis

preprocess_data:
  stage: data_preprocessing
  script:
    - python preprocess_data.py raw_data.csv cleaned_data.csv

run_analysis:
  stage: analysis
  script:
    - python analyze_data.py cleaned_data.csv results.csv
```
{% else %}
CI/CD tools automate workflows that run analyses to ensure consistent testing and result regeneration.
{% endif %}
:::

:::{card} 5. **Documentation**
{% if page %}
Tools like GitHub and GitLab provide ways to document workflows using README files, wikis, or markdown-based documentation. Clear instructions on how to clone the repository, set up the environment, and run the analysis help ensure that others can reproduce the results.
{% else %}
Document workflows for reproducibility using Wikis, or `*.md`-based documentation.
{% endif %}
:::

:::{card} 6. **Traceability: Tracking Ideas, Development, and Changes**
{% if page %}
Traceability goes beyond reproducibility by not only ensuring that an experiment or analysis can be repeated with the same inputs and processes to get the same results but also by providing full visibility into the entire development process, including the reasoning behind changes, decisions, and workflows.

Remote services like **GitHub** and **GitLab** offer built-in tools like **issues**, **merge requests** (GitLab), **pull requests** (GitHub), and **news feeds** that help track the development process. These tools allow you to associate code changes with specific ideas or goals, providing a clear narrative that helps others understand how decisions were made and why certain changes occurred.

**Example: Traceability Workflow in GitLab**

- **Issue Tracking**: Log new ideas or bugs that need to be addressed.
- **Merge Requests**: Review code changes linked to specific issues.
- **Commit History**: Track every commit, showing which issue or merge request prompted the change.
{% else %}
Providing full visibility into the entire development process.
{% endif %}
:::
