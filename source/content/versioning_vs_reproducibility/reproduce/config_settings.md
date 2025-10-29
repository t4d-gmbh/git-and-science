{% if slide %}####{%else%}:::{card}{%endif%} Configuration Settings
Involves documenting parameters and settings that guide the analysis, which is essential for reproducing the same results.

```{note}
This includes **randomness control**, i.e., the use and specification of seeds whenever possible.
```

**How?**

- Declare **all** configuration parameter **separately** from your analysis scripts!
- Use simple and readable formats (e.g. `.YAML` or `.json`).
- Track the configuration files in the same repository as your analysis scripts.

```{hint}
If you use multiple machines, maintain separate configuration files for each.
This way, you avoid manually updating settings in your scripts when switching machines.
```
{%if page %}:::{%endif%}


