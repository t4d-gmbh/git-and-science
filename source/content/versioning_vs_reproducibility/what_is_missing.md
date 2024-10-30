### What’s Missing for Reproducibility in Git Version Control

:::{card}
### Data Versioning
{% if page %}
Git is optimized for versioning code, which typically consists of small text files. However, scientific projects often involve large datasets, which Git cannot handle efficiently. Large files or datasets can cause performance issues and aren't inherently tracked in Git.
{% else %}
Git can not efficiently handle large binary files or datasets.
{% endif %}
:::
:::{card}
### Environment Consistency
{% if page %}
Even if you version your code, it's crucial to ensure that the software environment (e.g., dependencies, libraries, and versions of tools) used to run that code is the same when the project is re-run. Git does not inherently track environment dependencies, and subtle differences in the software stack can lead to different results.
{% else %}
Git does not inherently track environment dependencies, which can lead to different results.
{% endif %}
:::

:::{card}
### Execution Order and Workflow
{% if page %}
Git manages code changes but doesn’t track the workflow or the order in which scripts are run. A clear workflow is essential for reproducibility to ensure that others know how to replicate the results step by step.
{% else %}
Git doesn’t track the workflow or the order in which scripts are run.
{% endif %}
:::

:::{card}
### Data and Code Separation
{% if page %}
Data is often stored separately from the code, either due to size or organizational reasons. While Git can track submodules (other repositories), it doesn't automatically handle the separation and re-aggregation of data repositories and analysis code. This separation can hinder reproducibility if not properly managed.
{% else %}
Git doesn't automatically handle the separation and re-aggregation of data repositories and analysis code.
{% endif %}
:::

:::{card}
### Automation
{% if page %}
Reproducibility also involves automating the execution of analysis, including triggering code execution when data or code changes. Git does not have native automation capabilities for running workflows.
{% else %}
Git does not have native automation capabilities for running workflows.
{% endif %}
:::
