## Use Cases for Submodules
{% if build == "pages" %}

### Third-party Libraries

If you are developing a project that relies on third-party libraries, you can use submodules to include these libraries in your project. 
This way, you can keep your project and the libraries separate, making it easier to manage updates and changes.
For example, you might use a submodule to include a the code of a paper you want to integrate in your analysis.

### Shared Code

If you have a common codebase that is used across multiple projects, you can create a submodule for this codebase.
This way, you can make changes to the shared codebase and have those changes reflected in all the projects that use it.
For example, you might have a library of functions that are used in multiple projects. By creating a submodule for this library, you can update the library in one place and have the changes propagate to all the projects that use it.

### Separate Repositories

If you have a project that is made up of multiple repositories, you can use submodules to link these repositories together.
This way, you can manage the different parts of your project separately while still being able to work on them together.
For example, this course is made up of multiple repositories, each containing different parts of the course content.

```bash
using-git-in-accademia
├── ci-cd-workflows
├── git-and-science
├── git-and-its-remotes
├── working-with-git
```

{% else %}

{% endif %}