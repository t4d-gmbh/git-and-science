### Bringing It All Together: Enhancing Reproducibility

To go from basic version control to full reproducibility, you need:

1. **Documentation**: Include documentation into the repository (`README.md` or `docs/`)
1. **Data Availability**: Publish data! Use <i class="fab fa-git"></i> LFS for versioning
1. **Workflow Documentation**: Use <i class="fab fa-git"></i> submodules and automation scripts to declare the full analysis workflow.
1. **Dependencies**: Specify direct dependencies.
1. **Transitive Dependencies**: Define isolated execution environments.
1. **Environment tracking**: Use isolation tools like Docker or ✨NixOS✨.
1. **Configuration Settings**: Declare and load configurations.
