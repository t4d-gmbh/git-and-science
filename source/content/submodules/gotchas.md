## Gotchas for <i class="fab fa-git"></i> Submodules

1. **Submodules Do Not Update Automatically** ⚠️:
{% if slide %}
Submodules are not automatically updated to the latest commit.
{% else %}
When you clone a repository that contains submodules, the latter are not automatically updated to the latest commit. You need to run `git submodule update` or use the `--recurse-submodules` option when cloning to ensure they are initialized and updated.
{% endif %}

2. **Repository Resides in the `.git` Folder of the Parent Repo** 🔒: The metadata for submodules is stored in the parent repository's `.git` folder.
{% if page %}
This means that the actual repository for the submodule is not in its own separate `.git` folder, which can lead to confusion. Be cautious that providing access to the parent repository's `.git` folder grants access to the history of all its submodules!
{% endif %}

3. **Submodule Commits Are Detached** 🤔: <i class="fab fa-git"></i> submodules are designed to be pinned to a specific commit and do not track a branch.
{% if page %}
When you check out a submodule, it is usually in a "detached HEAD" state, generally meaning it is not on a branch. This can be confusing if you try to make changes directly in the submodule without creating a new branch first.

   :::{tip}
   You can set up a submodule to track a branch with the `-b` option:
   
   ```bash
   git submodule add -b <bname> https://gitlab.com/...
   ```
   Alternatively, navigate into the directory of an existing submodule (e.g., `mySub`) and run:
   ```bash
   git checkout bname
   git branch --set-upstream=origin/bname
   cd ../  # you leave the submodule
   git add mySub
   git commit -m "Tracking branch bname in mySub"
   ```
   :::

{% endif %}

4. **Submodule URLs Can Change** 🔗:
{% if slide %}
You might need to update the `.gitmodules` file manually.
{% else %}
If the URL of a submodule repository changes, you must update the `.gitmodules` file in the parent repository. Failing to do so can lead to broken links when trying to update or clone the submodule.
{% endif %}

5. **Cloning with Submodules Requires Extra Steps** 🛠️:
{% if slide %}
Remember to use the `--recurse-submodule` option when cloning.
{% else %}
When cloning a repository with submodules, you need to use the `--recurse-submodules` option or run `git submodule init` and `git submodule update` afterward. Forgetting these steps can lead to missing submodule content.
{% endif %}

6. **Submodules Can Increase Complexity** 🌀:
{% if slide %}
This might be confusing for newcomers.
{%else%}
Using submodules can add complexity to your project structure. If not managed properly, it can lead to confusion about which version of a submodule is being used and how it relates to the parent repository.
{% endif %}
