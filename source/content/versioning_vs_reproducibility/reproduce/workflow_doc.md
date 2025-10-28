{% if slide %}####{%else%}:::{card}{%endif%} Workflow Documentation
Clearly document the steps taken in the analysis to allow others to understand and replicate the process.

**How?**

- Document the execution workflow in an automation script. E.g., with a simple `run_analysis.sh`, a workflow management tool like [_snakemake_](https://snakemake.readthedocs.io/en/stable/) or [_nextflow_](https://www.nextflow.io/), or GitHub Actions {octicon}`play;0.8em`.
- Clarify how the version of the analysis scripts, as well as, the datasets are linked to the execution of the analysis.
- Specify how the execution environment is built up.

{%if page %}:::{%endif%}
