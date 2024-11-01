## How <i class="fab fa-git"></i> Can Enhance Reproducibility
{% if slide %}
- **Version Control**: Track and version your analysis scripts with <i class="fab fa-git"></i>.
  
- **Dependency Management**: 
  - Add files like `renv.lock` or `pyproject.toml` to pin dependencies.
  
- **Documentation**: 
  - Use a `README.md` to outline installation, running instructions, and workflow insights.

- **Parameterization**: 
  - Include a parameter file (e.g., `.YAML` or `.json`) to document settings and load them in your script.
{% else %}
By using <i class="fab fa-git"></i>, you can effectively track and version the scripts associated with your computational analysis.
You can easily add a simple text file (such as `renv.lock` or `pyproject.toml`) that contains pinned direct dependencies to your repository, allowing them to be tracked alongside the rest of your code.
This establishes a solid foundation for managing **dependencies** directly with <i class="fab fa-git"></i>.

Utilizing a standard `README.md` file enables you to document the installation process for declared dependencies, instructions for running the analysis script, and provide insights into how the **analysis workflow** is structured and should be executed.

Moreover, incorporating a parameterization file (e.g., a `.YAML` or `.json` file) into the repository allows you to outline the parameters utilized in the analysis.
Ideally, you should modify the analysis script to automatically load all necessary parameters from this file.
This approach facilitates documentation and tracking the **configuration settings** employed in your analysis, including random number generator seeds, hyperparameters, and more.
{% endif %}
