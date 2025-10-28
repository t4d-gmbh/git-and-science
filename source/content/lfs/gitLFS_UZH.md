## <i class="fab fa-git"></i> LFS Availability at UZH

{% if build == "pages" %}
Popular <i class="fab fa-git"></i> hosting services like GitHub, GitLab, Bitbucket, and Azure DevOps have built-in support for <i class="fab fa-git"></i> LFS.

For self-hosted <i class="fab fa-git"></i> servers, it is important to ensure <i class="fab fa-git"></i> LFS support is enabled. This may require additional installation and configuration because <i class="fab fa-git"></i> LFS stores large files in a separate storage location, which requires extra server-side support management (e.g., storage, authentication, bandwidth handling).

At the IMATH, <i class="fab fa-git"></i> LFS is **NOT supported** on the [IMATH GitLab](https://gitlab.imath.uzh.ch) instance.

However, at the University of Zurich (UZH), <i class="fab fa-git"></i> LFS is supported on the [UZH GitLab](https://gitlab.uzh.ch) instance, with a **size limit of 15 GB per project** (this includes all parts of a project, i.e. <i class="fab fa-git"></i> repository, LFS, etc.). 
The data is stored in the [Switch Cloud](https://www.switch.ch/en/competencies/cloud), which is hosted outside UZH but remains within Switzerland, though generally the UZH data protection regulations still apply.

Please note that GitLab is primarily intended for collaborative software development, not simply for data storage. 
UZH's GitLab has limited disk space, and all data is deleted after 12 months of user inactivity. 
For long-term data storage, it is recommended to use [OneDrive](https://uzh-my.sharepoint.com/my) or [SwitchDrive](https://drive.switch.ch/).

{% else %}

- Popular <i class="fab fa-git"></i> hosting services like GitHub, GitLab, and Bitbucket support <i class="fab fa-git"></i> LFS.
- Self-hosted <i class="fab fa-git"></i> servers require additional configuration to enabel <i class="fab fa-git"></i> LFS.
- <i class="fab fa-git"></i> LFS is **supported** on the [IMATH GitLab instance](https://git.math.uzh.ch/).
- <i class="fab fa-git"></i> LFS is **supported** on the [UZH GitLab instance](https://gitlab.uzh.ch/).
  - **Size Limit**: 15 GB per project.
  - **Data Storage**: [Switch Cloud](https://www.switch.ch/en/competencies/cloud) (Switzerland).
  - **Data Retention**: Data is deleted after 12 months of inactivity.

{% endif %}
