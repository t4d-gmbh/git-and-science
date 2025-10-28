{% if slide %}####{%else%}:::{card}{%endif%} Transitive Dependencies {octicon}`package-dependencies`{octicon}`package-dependencies;0.8em`{octicon}`package-dependencies;0.6em`{octicon}`package-dependencies;0.4em`
Address the indirect dependencies required by your primary libraries.
Managing this ensures that all necessary components are accounted for.

**How?**

- Utilize isolated, temporary environments to execute your analysis. E.g., [_virtualenv_](https://virtualenv.pypa.io/en/latest/), [_renv_](https://rstudio.github.io/renv/articles/renv.html) or [_conda_](https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html    ).
- Prefer declarative systems such as [_NixOS_](https://nixos.org/), or at the very least, use [Docker <i class="fa-brands fa-docker"></i>](https://www.docker.com/).

{%if page %}:::{%endif%}

