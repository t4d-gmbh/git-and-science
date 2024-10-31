{% if slide %}####{%else%}:::{card}{%endif%} Dependencies {octicon}`package-dependencies`
Refers to the libraries and frameworks used in the analysis.
Specifying exact versions helps control for changes that could affect results.

**How?**

- Include dependency declarations in your <i class="fab fa-git"></i> repository. E.g. `requirements.txt` or `environment.yml`.
- **Pin** dependencies rather than minimal requirements. E.g., `numpy==1.19.2` instead of `numpy>=1.19.2`.

{%if page %}:::{%endif%}
