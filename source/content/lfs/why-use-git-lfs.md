## Why Using <i class="fab fa-git"></i> LFS?

{% if build == "pages" %}
Data management is a critical aspect of scientific research and is often not versioned or tracked leading to data loss, duplication, or errors.

Tracking large files with <i class="fab fa-git"></i> can be challenging. 
As the size of your repository grows, it can slows down the <i class="fab fa-git"></i> operations, such as cloning, fetching, and pushing because <i class="fab fa-git"></i> stores the entire history of the repository locally.
To address this issue, <i class="fab fa-git"></i> Large File Storage (LFS) provides a solution for managing large files in your <i class="fab fa-git"></i> repositories.

Git Large File Storage (LFS) is a <i class="fab fa-git"></i> extension that replaces large files in your repository with text pointers while storing the file contents on a remote server. 
This approach allows you to work with large files in your repository without slowing down the <i class="fab fa-git"></i> operations.

{% else %}

- **Data Management**: Proper data management is crucial in scientific research to prevent data loss, duplication, and errors.
- **Efficiency**: Traditional <i class="fab fa-git"></i>  struggles with large files, leading to slow performance and bloated repositories.
- **Collaboration**: Ensures team members can work with large files without conflicts or performance issues.
- **History Tracking**: Maintains a history of changes, making it easier to revert to previous versions if needed.

{% endif %}
