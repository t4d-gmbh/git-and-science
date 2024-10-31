{% if slide %}####{%else%}:::{card}{%endif%} Configuration Settings
Involves documenting parameters and settings that guide the analysis, which is essential for reproducing the same results.

:::{note}
This includes **randomness control**, i.e. the usage and specification of seeds whenever possible.
:::

**How?**

- Declare **all** configuration parameter **separately** from your analysis scripts!
- Use simple and readable formats (e.g. `.YAML` or `.json`).
- Track the configuration files in the same repository as your analysis scripts.

{%if page %}:::{%endif%}


