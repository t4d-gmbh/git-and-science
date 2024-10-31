{% if slide %}####{%else%}:::{card}{%endif%} Transitive Dependencies
Addresses the indirect dependencies required by your primary libraries.
Managing these ensures that all necessary components are accounted for.

**How?**

- Utilize isolated, temporary environments to execute your analysis.
- Prefer declarative systems such as _NixOS_, or at the very least, use Docker.

{%if page %}:::{%endif%}

