## Exercise: The Course Content Structure

{% if page %}
Now that we know about Git submodules, let's take a closer look at how the material of this course is actually structured and how the web-content is built.

{% endif %}
Each of the 4 parts of this course resides in its own Repository:

::::{grid} 2 2 2 2
:gutter: 3

:::{grid-item-card} {octicon}`repo;1em` Part1: Working with Git
:class-header: sd-bg-warning sd-text-white
**<https://github.com/t4d-gmbh/working-with-git>**
:::

:::{grid-item-card} {octicon}`repo;1em` Part2: Git and its remotes
:class-header: sd-bg-warning sd-text-white
**<https://github.com/t4d-gmbh/git-and-its-remotes>**
:::

:::{grid-item-card} {octicon}`repo;1em` Part 3: CI/CD Workflows
:class-header: sd-bg-warning sd-text-white
**<https://github.com/t4d-gmbh/ci-cd-workflows>**
:::

:::{grid-item-card} {octicon}`repo;1em` Part 4: Git and Science
:class-header: sd-bg-warning sd-text-white
**<https://github.com/t4d-gmbh/git-and-science>**
:::
::::

{% if page %}
In this main course Repository (**<https://github.com/t4d-gmbh/using-git-in-academia>**) all the content is aggregated, compiled into `html`, and published as a [GitHub page](https://docs.github.com/en/pages).
However, the content of the four parts does not reside directly in the main course **<https://github.com/t4d-gmbh/using-git-in-academia>** Repository itself:
{% else %}
In **<https://github.com/t4d-gmbh/using-git-in-academia>** the four parts are combined and the `html` pages are built.
{% endif %}

::::{grid} 1 1 2 2
:gutter: 3

:::{grid-item-card} {octicon}`question;1em` Key Questions
:class-header: sd-bg-warning sd-text-white

- How are the four parts included into the main course repository (**<https://github.com/t4d-gmbh/using-git-in-academia>**)?
- What are the advantages of such a setup?
- What are potential drawbacks?

:::

:::{grid-item-card} {octicon}`light-bulb;1em` Hint
:class-header: sd-bg-info sd-text-white

- Have a look at the `source/content` folder in the main course repository (**<https://github.com/t4d-gmbh/using-git-in-academia>**).
- The `source/index.md` file declares what is included in the `html` content.
:::
::::

{% if page %}
---

::: {admonition} How the 4 parts are included
:class: tip, dropdown

The four parts are handled as submodules and added in the `source/content/` directory.
This is specified in the [`.gitmodules`](https://github.com/t4d-gmbh/using-git-in-academia/blob/main/.gitmodules) file that has entries in the form:

```toml
[submodule "source/content/working-with-git"]
	path = source/content/working-with-git
	url = https://github.com/t4d-gmbh/working-with-git.git
	branch = main
```

With this setup we can fetch the content of the submodules (e.g. with `git submodule update --remote`) "unpacking" the content of the repositories into the specified paths.

The actual import of the content is then initiated in the `source/index.md` file with an import block like this (simplified):

```markdown 
\```{toctree}
:caption: Part 1: Working with Git
:maxdepth: 1
:numbered:
:hidden:

content/working-with-git/source/content/index
\```
```

Finally, the process is automated in the `pages.yml` workflow, that fetches the four submodules for us (see [relevant lines](https://github.com/t4d-gmbh/using-git-in-academia/blob/5e814c73b3b31b1311b54a8be37976f3da465c83/.github/workflows/pages.yml#L34-L35)), builds the pages and the slides ([here](https://github.com/t4d-gmbh/using-git-in-academia/blob/5e814c73b3b31b1311b54a8be37976f3da465c83/.github/workflows/pages.yml#L41-L46)) and deploys the generated `html` content to a static page ([here](https://github.com/t4d-gmbh/using-git-in-academia/blob/5e814c73b3b31b1311b54a8be37976f3da465c83/.github/workflows/pages.yml#L47-L55)).
:::

:::{admonition} Advantages of such a setup
:class: tip, dropdown

With submodules, we can **decouple the content of each part** from each other and the main course (**<https://github.com/t4d-gmbh/using-git-in-academia>**).
This allows for independent development in each part without affecting the others and the combined content.

In addition, each version of the combined content (i.e. each commit in **<https://github.com/t4d-gmbh/using-git-in-academia>**) specifies the exact version (i.e. the commit hash) of each of the four parts included.
Thus, whenever we "checkout" a specific commit in the `using-git-in-academia` repository, we will also get the specific versions of the four parts.

Furthermore, we can **decide for each part individually which version we want to use**. We simply set the submodule to the state we want and create a new tag in the main repository.

Finally, the **parts can be viewed on their own**, see e.g. [t4d-gmbh.github.io/working-with-git/](https://t4d-gmbh.github.io/working-with-git/) or recombined differently.

:::

:::{admonition} Potential disadvantages
:class: tip, dropdown

Using **Git submodules generally adds a layer of complexity** to a project, which makes it more difficult to handle, especially for collaborators providing smaller contributions.
Splitting up the content into four different repositories and providing the actual `html` content from a fifth repository, that simply aggregates the four parts obstructs a simple mapping from the individual `html` pages to the markdown files that define them.

An additional drawback of submodules can be the decoupling of versions:
A **change in any of the submodules is not automatically picked up** when running `git submodule update` in the main repository.
By default, a git submodule always stays at the specified commit hash.
This is a big advantage when it gets to consistency, however, in some cases this behaviour is not what we want, and we might accidentally display some outdated content if we forget to update the status of a submodule.

One approach to address this issue is by specifying a `branch` for each submodule (in the `.gitmodules` file) and to update them with `git submodule update --remote`.
The `--remote` option will ensure that the latest commit of the specified branch is used and not the currently registered one.

:::

{% endif %}
