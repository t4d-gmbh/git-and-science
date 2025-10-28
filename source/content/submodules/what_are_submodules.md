## What are <i class="fab fa-git"></i> Submodules <i class="fa-solid fa-folder-tree"></i>?
{% if slide %}
- A [<i class="fab fa-git"></i> submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules) <i class="fa-solid fa-folder-tree"></i> is a **repository within another repository**.
- It helps to **manage external repositories in your main project**.
- They are useful for **including third-party libraries or separately maintained dependencies**.
{% else %}
A <i class="fab fa-git"></i> submodule is essentially a repository embedded within another repository. 
It allows you to include and manage external repositories within your main project. 
This is particularly useful for integrating third-party libraries or dependencies that are maintained separately.
{% endif %}

:::{note}
Once a submodule is initialized and updated, its content appears as a regular folder inside the parent repository.
:::

{% if page %}

### Why are Submodules Useful?

When working on a project, you may need to incorporate another project, such as a library developed by someone else or a tool you're building for use in multiple projects.
A common challenge in these situations is maintaining separation between the two projects separate while being able to use one with the other.

For example, imagine you're conducting research and want to use a data analysis tool you previously developed for another project.
You have two options: you could copy the code from the old project into your new one, or you could include it from a shared source. 
The problem with copying the code is that if you make any changes, it can be difficult to merge those changes back into the original tool later.
Conversely, including it from a shared source may limit your ability to customize it, and ensuring that all collaborators have access to it can be challenging.

<i class="fab fa-git"></i> addresses this issue with something called submodules.
Submodules allow you to keep a <i class="fab fa-git"></i> repository as a subfolder within another <i class="fab fa-git"></i> repository.
This setup enables you to selectively include specific versions of external repositories in your main project.
This is particularly useful for incorporating your own tools or third-party resources that are maintained separately, while allowing you to keep your changes separate.
{% endif %}
