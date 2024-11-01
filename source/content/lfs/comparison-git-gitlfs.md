## <i class="fab fa-git"></i> vs. <i class="fab fa-git"></i> LFS: A Comparison

{% if build == "pages" %}

### <i class="fab fa-git"></i> 

When you commit changes with <i class="fab fa-git"></i>, it creates objects to represent the state of your files at that point in time, which are stored in the `.git/objects` directory.
Each object is a snapshot of the file contents, and <i class="fab fa-git"></i>  uses pointers (hashes) to reference these objects.

<i class="fab fa-git"></i>  is optimized for handling text files.
Since text files typically have small, incremental changes, <i class="fab fa-git"></i> efficiently stores only the differences (deltas) between versions.

However, changes in binary files (e.g., images, videos, datasets) are not as easily represented as deltas.
When a binary file is modified, <i class="fab fa-git"></i>  often stores the entire file again, leading to bloated repositories and slower performance over time.

### <i class="fab fa-git"></i> LFS

<i class="fab fa-git"></i> LFS replaces large files with small pointer files that 
reference the actual content stored outside the main repository.

The large files themselves are stored in a seperate location (e.g., a remote server) which keeps the main repository lightweight and efficient.
When you clone a repository using <i class="fab fa-git"></i> LFS, only the pointer files are downloaded, not the large files.
When you checkout a file, <i class="fab fa-git"></i> LFS automatically downloads the actual file content.
Similarly, when you commit a large file, <i class="fab fa-git"></i> uploads it to the external storage and replaces it with a pointer file in the repository.

{% else %}

| <i class="fab fa-git"></i>  | <i class="fab fa-git"></i> LFS |
|:---:|:-------:|
| Optimized for text files | Optimized for large files |
| Stores entire file contents locally | Stores large files externally |
| Performance slows with large files | Maintains repository performance with large files |
| Leads to bloated repositories | Keeps repositories lightweight |

{% endif %}
