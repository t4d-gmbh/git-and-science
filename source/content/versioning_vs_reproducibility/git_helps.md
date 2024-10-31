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
You can easily add a simple text file (such as `renv.lock` or `pyproject.toml`) that contains pinned direct dependencies to your repository, allowing it to be tracked alongside the rest of your code.
This establishes a solid foundation for managing **dependencies** directly with <i class="fab fa-git"></i>.

In a similar fashion, utilizing a standard `README.md` file enables you to document the installation process for the declared dependencies, instructions for running the analysis script, and provide insights into how the **workflow** of the analysis is structured and should be executed.

Moreover, you can incorporate a parameterization file (e.g., a `.YAML` or `.json` file) into the repository that outlines the parameters utilized in the analysis.
Ideally, you should modify the analysis script to automatically load all necessary parameters from this file.
This approach allows you to document and track the **configuration settings** employed in your analysis, including random number generator seeds, hyperparameters, and more.
{% endif %}
