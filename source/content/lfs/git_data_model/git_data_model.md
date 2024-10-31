## How does git Track Files?

To understand how Git LFS works, it's essential to first understand how Git tracks files.

One of the core functionalities of Git is its ability to track files and their changes efficiently. 
But how does the underlying mechanisms and data structures look like?

### Git’s Data Model
Git’s data model is based on three main concepts: 

**Blobs (Binary Large Objects):**
They are used to store the contents of files. 
Each blob is identified by a SHA-1 hash of its content, ensuring that identical files are stored only once.
Blobs do not contain any metadata about the file, such as its name or permissions.

**Trees:**
represent directories and contain pointers to blobs (files) and other trees (subdirectories).
Each tree object includes the file names, permissions, and the SHA-1 hashes of the blobs or trees it contains.

**Commits:**
are snapshots of the entire repository at a given point in time.
A commit object contains a pointer to a tree object (representing the state of the repository), metadata (such as the author, committer, and commit message), and pointers to parent commits.

### Tracking Changes
Git tracks changes to files through a series of stages:

**Working Directory:**
This is where you make changes to your files.
Git does not track these changes until you stage them (recall, git works asynchronically).

**Staging Area (Index):**
The staging area is a file (usually located in .git/index) that stores information about what will go into your next commit.
When you stage a file using `git add`, Git calculates the SHA-1 hash of the file’s content, creates a blob object if it doesn’t already exist, and updates the index with the blob’s hash and the file’s metadata.

**Repository (History):**
When you commit changes, Git creates a new commit object that points to the current state of the staging area.
The commit object is added to the repository’s history, forming a chain of commits that represent the project’s evolution over time.

### Efficient Storage
Git uses several techniques to efficiently store and manage file changes:

**Delta Compression:**
Git uses delta compression to store the differences between file versions.
Delta compression is particularly effective for text files, where changes are often small and incremental (e.g., adding a line of code).
When you commit a change, Git calculates the delta (difference) between the new file and the previous version by comparing the blobs’ content.

**Object Hashing:**
Git uses SHA-1 hashing to identify objects (blobs, trees, commits) in the repository.
The SHA-1 hash is a unique identifier generated from the object’s content, ensuring that identical objects have the same hash.
This mechanism allows Git to store objects efficiently and avoid duplicate content.

**Packfiles:**
Git stores objects in packfiles to reduce disk space and improve performance.
Packfiles are compressed files that contain multiple objects (blobs, trees, commits) and are created using Git’s garbage collection process.
When you push changes to a remote repository, Git creates packfiles to transfer the objects efficiently.

In summary, Git’s ability to track files and manage changes efficiently is a result of its robust data model and storage mechanisms.
By using blobs, trees, and commits, Git ensures that file contents are stored uniquely and changes are tracked accurately. 
The staging area and efficient storage techniques like delta compression and packfiles contribute to Git’s performance and reliability as a version control system.
