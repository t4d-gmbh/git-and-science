## Essential Commands

Here’s a simple overview of the basic commands for working with <i class="fab fa-git"></i> submodules:

| Command                                      | Description                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| `git submodule add <rep-url> [path]` | Add a new submodule to the project.                                                                     |
| `git submodule update --init --remote`      | Initialize & update, fetching the latest changes from remote repo.                               |
| `git submodule update`                      | Update the submodules to the commit specified in the parent repo.                                |
| `git submodule update --remote [path]`      | Update the submodule to the latest commit on the tracked branch.                                 |
| `git submodule status [path]`               | Check the status of the submodules (in [path]).                                                  |
| `git rm --cached [path-to-submodule]`       | Remove a submodule from the parent repository.                                                   |
