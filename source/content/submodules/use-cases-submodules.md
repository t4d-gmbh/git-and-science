## Use Cases
{% if build == "pages" %}

### Third-party Libraries

If you are developing a project that relies on third-party libraries, you can use submodules to include these libraries in your project without merging them directly into your project. 
This makes it easier to manage updates and changes.
For example, you might use a submodule to include the code of a research paper you want to integrate into your analysis.

### Shared Code

If you have a common codebase that is used across multiple projects, submodules can help you centralize and streamline updates. By creating a submodule for this shared codebase, any changes made will automatically be reflected in all dependent projects.
For example, if you have a library of functions that are used in multiple projects, a submodule allows you to update it in one place and propagate those changes to all the projects that depend on it.

### Separate Repositories

For projects that consist of multiple repositories, submodules allow you to link these repositories together while maintaining separate version control for each.
This allows for modular project management while still working on them cohesively.
For example, this course is organized into several repositories, each containing different sections of the course material.

```bash
using-git-in-accademia
├── ci-cd-workflows
├── git-and-science
├── git-and-its-remotes
├── working-with-git
```

{% else %}

Submodules can be used in a various scenarios for managing complex projects. Common use cases include:

1. **Third-party Libraries {octicon}`package-dependencies`**: Incorporating external libraries or dependencies into your project.
2. **Shared Code {octicon}`share-android;0.8em`**: Centralizing a codebase that multiple projects rely on.
3. **Separate Repositories <i class="fa-solid fa-folder-tree"></i>**: Managing multiple repositories for different parts of a project while keeping them linked.

{% endif %}
