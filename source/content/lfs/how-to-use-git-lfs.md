## How to use <i class="fab fa-git"></i> LFS

{% if build == "pages" %}

To use <i class="fab fa-git"></i> LFS, you need to install the <i class="fab fa-git"></i> LFS client on your local machine.

### 1. Install Git LFS:
   - Download and install from [git-lfs.github.com](https://git-lfs.github.com).
   - Initialize in your repository by running the following command in your repository directory:
     ```bash
     git lfs install
     ```

### 2. Track Large Files:
   - Specify the file types to be tracked by <i class="fab fa-git"></i> LFS. For example, to track all `.pdf` files, run:
     ```bash
     git lfs track "*.pdf"
     ```

### 3. Commit and Push:

- Add the `.gitattributes` file:

  The `.gitattributes` file is a configuration file used by <i class="fab fa-git"></i> to manage attributes for paths in your repository.
  It allows you to define how certain files should be handled by <i class="fab fa-git"></i>, including aspects like line endings, mark files as binary to prevent text-based operations on them, and more. 
  This file is particularly useful when working with <i class="fab fa-git"></i> LFS to specify which files should be managed by LFS.

  ```bash
  git add .gitattributes
  ```

  Example: 
  If you want to use Git LFS for large media files like images and videos, your `.gitattributes` file might look like this:

  ```bash
  # Use LFS for image files
  *.jpg filter=lfs diff=lfs merge=lfs -text
  *.png filter=lfs diff=lfs merge=lfs -text

  # Use LFS for video files
  *.mp4 filter=lfs diff=lfs merge=lfs -text
  ```

- Add, commit, and push large files:
  ```bash
  git add <large-file>
  git commit -m "Add large file"
  git push
  ```

{% else %}

- Install Git LFS from [git-lfs.github.com](https://git-lfs.github.com) and initialize it with `git lfs install`.
- Track large files by specifying file types, e.g., `git lfs track "*.pdf"`.
- Add the `.gitattributes` file to manage file attributes and specify LFS management for certain files.
    Example `.gitattributes` entries for images and videos:
    ```bash
    *.jpg filter=lfs diff=lfs merge=lfs -text
    *.png filter=lfs diff=lfs merge=lfs -text
    *.mp4 filter=lfs diff=lfs merge=lfs -text
    ```
- Add, commit, and push large files using Git LFS.

{% endif %}

