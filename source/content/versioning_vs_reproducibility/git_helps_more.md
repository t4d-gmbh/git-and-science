## <i class="fab fa-git"></i> Can Do More!
{% if slide %}
- **Handling Large Files**: 
  - <i class="fab fa-git"></i> is not ideal for tracking large binary files.

- **Git LFS Extension**: 
  - Use <i class="fab fa-git"></i> LFS to efficiently track and version larger datasets.

- **Data Availability**: 
  - Contribute to the **availability of analyzed data** by publishing the analyzed data along with the exact dataset version used in your analysis.
    - Use data repositories like [Zenodo](https://zenodo.org/), [Dryad](https://datadryad.org/), etc.
    - Publishers sometimes offer to publish the data in a separate data publication. E.g. [scientific data](https://www.nature.com/sdata/), [Data in Brief](https://www.sciencedirect.com/journal/data-in-brief), etc.
{% else %}
While tracking bigger files, an binary files in particular, is not <i class="fab fa-git"></i>'s strong suite there exists an extension, called <i class="fab fa-git"></i> LFS, that efficiently makes up for this shortcoming.

With <i class="fab fa-git"></i> LFS you can efficiently track and version even bigger dataset and thus contribute to the **availability of the analysed data** by publishing analyzed data, along with the exact version of the dataset that you used for your analysis.
{% endif %}
