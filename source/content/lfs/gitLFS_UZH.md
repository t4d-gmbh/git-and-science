## <i class="fab fa-git"></i> LFS Availability at UZH

{% if build == "pages" %}
Popular <i class="fab fa-git"></i> hosting services like GitHub, GitLab, Bitbucket, and Azure DevOps have built-in support for <i class="fab fa-git"></i> LFS.

In self-hosted <i class="fab fa-git"></i> server, it must be ensured that they have <i class="fab fa-git"></i> LFS support enabled which might come with installing and configuring additional software.

This is because <i class="fab fa-git"></i> LFS stores large files in a separate storage location, which requires additional server-side support to manage the large files (e.g., storage, authentication, bandwidth, etc.).

At the IMATH, <i class="fab fa-git"></i> LFS is NOT supported on the [IMATH GitLab](https://gitlab.imath.uzh.ch) instance.

<!-- At the University of Zurich (UZH), <i class="fab fa-git"></i> LFS is supported on the [UZH GitLab](https://gitlab.uzh.ch) instance. -->

{% else %}

- <i class="fab fa-git"></i> hosting services like GitHub, GitLab, and Bitbucket support <i class="fab fa-git"></i> LFS.
- Self-hosted <i class="fab fa-git"></i> servers need additional configuration for <i class="fab fa-git"></i> LFS.
- <i class="fab fa-git"></i> LFS is _not_ supported on the [IMATH GitLab instance](https://git.math.uzh.ch/).

{% endif %}