## Working with <i class="fab fa-git"></i> Submodules

{% if slide %}
- First **checkout a branch in the submodule** since it typically operates in "detached HEAD" mode.
{%else%}
Remember that a submodule usually does not track a branch, so **before you start working in a submodule, checkout the branch you want to work on**!
{% endif %}

{% if slide %}
- Inside a submodule folder **work as if it were an ordinary <i class="fab fa-git"></i> repository**.
{%else%}
Once the submodule is initialized, you can **work inside the submodule folder as if it were an ordinary <i class="fab fa-git"></i> repository**.
{% endif %}

{% if slide %}
- To **update the tracked commit** for a submodule, check out the desired commit and then **add the submodule's path to a commit in the parent repository**.
{%else%}
After making any changes in a submodule, simply **add the path to the submodule to a commit** in the parent repository to **update the commit that the parent repository should track**.
{% endif %}
