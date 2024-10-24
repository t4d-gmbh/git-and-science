## Basic Submodule Workflow

### 1. **Adding a Submodule**
To add a submodule to your project, use the `git submodule add` command, specifying the repository you want to include and the directory where you want to store it.

**Example:**

```bash
# Add a submodule to the 'libs' directory
git submodule add https://github.com/username/external-library.git libs/external-library

# Initialize and update the submodule
git submodule update --init --recursive
```

This creates a `.gitmodules` file that stores the submodule's configuration.

### 2. **Cloning a Repository with Submodules**
When cloning a repository that contains submodules, you need to initialize the submodules to pull in their contents.

**Example:**

```bash
# Clone the parent repository with all submodules
git clone --recursive https://github.com/username/parent-repo.git

# Alternatively, if the repo was already cloned
git submodule update --init --recursive
```

### 3. **Updating a Submodule**
If the submodule has been updated in its own repository, you can pull those changes into the parent repository.

**Example:**

```bash
# Navigate into the submodule directory and pull changes
cd libs/external-library
git pull origin main

# Go back to the parent repository and commit the updated submodule reference
cd ../../
git add libs/external-library
git commit -m "Update submodule to latest version"
```

### 4. **Pinning a Submodule to a Specific Commit (for Reproducibility)**
To ensure reproducibility, you can pin the submodule to a specific commit, so your project always uses the same version of the submodule.

**Example:**

```bash
# Checkout a specific commit in the submodule
cd libs/external-library
git checkout <commit-hash>

# Go back to the parent repository and commit the submodule reference
cd ../../
git add libs/external-library
git commit -m "Pin submodule to specific commit"
```

This locks the submodule to the specific commit, ensuring consistency across different environments.

### 5. **Removing a Submodule**
If you need to remove a submodule, you can do so with the following commands:

**Example:**

```bash
# Deinitialize the submodule
git submodule deinit -f -- libs/external-library

# Remove the submodule's entry in the .gitmodules file
git rm -f libs/external-library

# Remove the submodule directory
rm -rf .git/modules/libs/external-library
```
