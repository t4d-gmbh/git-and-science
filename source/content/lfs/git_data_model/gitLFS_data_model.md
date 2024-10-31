## How <i class="fab fa-git"></i> LFS Tracks Large Files
{% if page %}
Git LFS (Large File Storage) is an extension to Git that improves the handling of large files. 
It replaces large files in your repository with lightweight references, while storing the actual file content on a remote server. 
{% endif %}

:::{card} How Git LFS Works
**Pointer Files:** {% if page %}
When you add a large file to a Git repository using Git LFS, the file is replaced with a small pointer file.
This pointer file contains metadata about the large file, such as its size and a unique identifier (OID - Object ID).
The pointer file is committed to the Git repository, while the actual large file is stored separately.
{% else %}
Git LFS replaces large files in a Git repository with small pointer files containing metadata, storing the actual files separately.
{% endif %}

**Storing Large Files:** {% if page %}
The actual content of the large file is stored on a remote LFS server. This server can be a dedicated LFS server, a cloud storage service, or any other storage solution that supports Git LFS.
When you push your changes to the remote repository, Git LFS uploads the large files to the LFS server and commits the pointer files to the Git repository.
{% else %}
The large files are stored on a remote LFS server.
{% endif %}

**Fetching Large Files:** {% if page %}
When you clone or pull a repository that uses Git LFS, the pointer files are downloaded as part of the Git repository.
Git LFS then automatically fetches the actual large files from the LFS server based on the pointers. This ensures that the large files are available locally without bloating the Git repository.
{% else %}
Cloning or pulling a repository with Git LFS, downloads the pointer files from the repository, and the large files are fetched from the LFS server as needed.
{% endif %}
:::

:::{card} Tracking Changes
{% if page %}
Git LFS tracks changes to large files in a way that integrates seamlessly with Git:
{% endif %}

**Adding Files:** {% if page %}
When you add a large file using `git lfs track`, Git LFS creates a `.gitattributes` file (if it doesn’t already exist) and adds an entry for the file type or specific file. This tells Git LFS to handle these files.
The large file is then added to the staging area, and a pointer file is created and committed to the repository.
{% else %}
Adding a large file with `git lfs track`, creates a `.gitattributes` file and adds an entry for the file type or specific file, telling Git LFS to manage these files.
{% endif %}

**Committing Changes:** {% if page %}
When you commit changes, the pointer file is included in the commit. The actual large file content is managed separately by Git LFS by uploading the large file to the LFS server and updating the pointer file with the OID (Object ID) of the large file.
This keeps the Git repository lightweight and ensures that large files do not slow down repository operations.
{% else %}
The pointer file is included in the commit, and the large file content is managed separately by Git LFS.
{% endif %}
:::

:::{card} Efficient Storage
{% if page %}
Git LFS optimizes storage and performance through several mechanisms:
{% endif %}

**Deduplication:** {% if page %}
Git LFS stores each unique version of a large file only once on the LFS server. 
If the same file is added multiple times, only one copy is stored, saving space.
{% else %}
Git LFS stores each unique version of a large file only once on the LFS server.
{% endif %}

{% if page %}
**Pointer Files:** By using pointer files, Git LFS reduces the size of the Git repository by storing large file metadata separately. This keeps the repository lightweight and improves performance.
{% endif %}

{% if page %}
**Bandwidth Optimization:** By storing large files separately and only downloading them when needed, Git LFS reduces the amount of data transferred during repository operations. This is particularly beneficial for teams working with large assets like media files or datasets.
{% endif %}
:::

{% if page %}
**Conclusion**
Git LFS enhances Git’s capabilities by efficiently managing large files. 
By using pointer files and storing large file content separately, Git LFS keeps repositories lightweight and performant. 
The integration with Git’s version control features ensures that large files are tracked and versioned seamlessly, making Git LFS a valuable tool for developers working with large assets.
{% endif %}