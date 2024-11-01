## Why Use <i class="fab fa-git"></i> LFS?

{% if build == "pages" %}
Effective data management is crucial in scientific research, yet it's often overlooked, leading to data loss, duplication, or errors.

Tracking large files with <i class="fab fa-git"></i> can be challenging. 
As the size of your repository grows, operations like cloning, fetching, and pushing can slow down because <i class="fab fa-git"></i> stores the entire repository's history locally.
To address this, <i class="fab fa-git"></i> Large File Storage (LFS) provides a solution for managing large files in your <i class="fab fa-git"></i> repositories.

<i class="fab fa-git"></i>-LFS is an extension that replaces large files in your repository with lightweight text pointers, while the actual file contents are stored on a remote server. 
This allows you to work with large files without affecting <i class="fab fa-git"></i> performance.

{% else %}

- **Data Management**: Proper data management is essential to avoid data loss, duplication, and errors in scientific research.
- **Efficiency**: Traditional <i class="fab fa-git"></i>  struggles with large files, leading to slow performance and bloated repositories.
- **Collaboration**: Enables team members to handle large files without conflicts or performance issues.
- **History Tracking**: Maintains a history of changes, making it easier to revert to previous versions when needed.

{% endif %}
