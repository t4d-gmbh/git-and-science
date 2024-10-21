## <i class="fab fa-git"></i> vs. <i class="fab fa-git"></i> LFS: A Comparison

{% if build == "pages" %}

### <i class="fab fa-git"></i> 

When you commit changes with <i class="fab fa-git"></i>, it creates objects to represent the state of your files at that point in time. 
These objects are stored in the `.git/objects` directory.
Each object is a snapshot of the file contents, and <i class="fab fa-git"></i>  uses pointers (hashes) to reference these objects.

<i class="fab fa-git"></i>  is optimized for text files.
Text files often have small, incremental changes, that <i class="fab fa-git"></i> can handle well by storing only the differences (deltas) between versions.

Changes in binary files (e.g., images, videos, datasets) are different from text files because changes are not easily represented as deltas.
When a binary file changes, <i class="fab fa-git"></i>  often stores the entire file again, leading to repository bloat and slow performance.

### <i class="fab fa-git"></i> LFS

<i class="fab fa-git"></i> LFS replaces large files with small pointer files. 
These pointer files reference the actual content stored outside the main repository.

The actual large files are stored in a seperate location (e.g., a remote server) which keeps the main repository lightweight and efficient.
When you clone a repository with <i class="fab fa-git"></i> LFS, you only download the pointer files, not the actual large files.
When you check out a file, <i class="fab fa-git"></i> LFS automatically downloads the large file content.
Similarly, when you commit a large file, <i class="fab fa-git"></i> uploads the large file to the external storage and replaces it with a pointer file in the repository.

{% else %}

| <i class="fab fa-git"></i>  | <i class="fab fa-git"></i> LFS |
|:---:|:-------:|
| Optimized for text files | Optimized for large files |
| Stores entire file contents | Stores large files externally |
| Slows down with large files | Maintains repository performance |
| Bloated repositories | Lightweight repositories |

{% endif %}