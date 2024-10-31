## Essential Commands for <i class="fab fa-git"></i> Submodules

Here’s a simple overview of the basic commands for working with <i class="fab fa-git"></i> submodules:

| Command                                      | Description                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------|
| `git submodule add <rep-url> [path]` | Add a new submodule to the project.                                                                     |
| `git submodule update --init --remote`      | Initialize & update, fetching the latest changes from remote repo.                               |
| `git submodule status [path]`               | Check the status of the submodules (in [path]).                                                  |
| `git submodule update --remote [path]`      | Update the submodule to the latest commit on the tracked branch.                                 |
| `git rm --cached [path-to-submodule]`       | Remove a submodule from the parent repository.                                                   |
| `git submodule init`                        | Initialize submodules in a cloned repository.                                                    |
| `git submodule update`                      | Update the submodules to the commit specified in the parent repo.                                |

Other than that, simply work inside the submodule folder as if it were an ordinary <i class="fab fa-git"></i> repository.
After any changes in a submodule, simply add the path to the submodule to a commit in the parent repository to update the commit the parent repository should track.
