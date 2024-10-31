# What are <i class="fab fa-git"></i> submodules <i class="fa-solid fa-folder-tree"></i>?

A git submodule is a <i class="fab fa-git"></i> repository embedded inside another <i class="fab fa-git"></i> repository. 

:::{note}
Once a submodule is initialized and updated, its content appears as a regular folder inside the parent repository.
:::

{% if page %}

### Why would you need that?

Sometimes, when you're working on a project, you might need to use another project within it.
This could be a library created by someone else or one that you're developing separately to use in multiple projects.
A common challenge in these situations is wanting to keep the two projects separate while still being able to use one inside the other.

For example, imagine you're conducting research and have previously developed a data analysis tool for another project.
Now, you want to use that same tool in your current research project.
You could either copy the code from the old project into your new one or include it from a shared source.
The problem with copying the code is that if you make any changes, it can be difficult to merge those changes back into the original tool later.
On the other hand, if you include it from a shared source, it can be hard to customize and ensure that everyone involved in the research has access to it.

<i class="fab fa-git"></i> addresses this issue with something called submodules.
Submodules let you keep an <i class="fab fa-git"></i> repository as a subfolder of another <i class="fab fa-git"></i> repository.
This allows you to selectively include specific versions of external repositories within your main project.
This is particularly useful for incorporating your own tools or third-party resources that are maintained separately, while still keeping your changes separate.
{% endif %}
