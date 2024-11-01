## Reproducibility
{% if slide %}

- **Reproducibility** is achieved when an analysis can be repeated using the same data, yielding the same results.
- **Replicability** occurs when an analysis with different data on the same study subject leads to the same conclusions.

> We focus on a strict interpretation of reproducibility: the same implementation of a method applied to the exact same data must produce the same result.

- This approach is common in computer science and can be supported by tools like <i class="fab fa-git"></i> and related remote services.

{% else %}

Before we begin, it is important to clarify the definition of "reproducibility" as opposed to "replicability".

In a scientific context, these terms are are often used interchangeably, but they can also refer to different concepts.

In this course, we adopt the widely accepted interpretation that reproducibility is achieved when an analysis can be repeated using the same data, yielding the same results.

Replicability, on the other hand, refers to the situation where an analysis conducted with different data on the same study subject leads to the same conclusions.

:::{note}
For an in-depth exploration of this subject, we recommend reading [Reproducibility and Replicability in Science](https://nap.nationalacademies.org/read/25303/chapter/6) (National Academies of Sciences, 2019)
:::

Based on these definitions, our focus here is on a narrow interpretation of reproducibility. More specifically we consider reproducibility when the same implementation of a method applied to the exact same data produces the same result, as it is commonly adopted in computer science.
We will demonstrate how <i class="fab fa-git"></i> and related remote services can be utilized to enhance the reproducibility of computational studies in this sense.
{% endif %}

:::{attention}
Some products require strict certification processes, such as the [ASME VVUQ standard](https://www.asme.org/codes-standards/publications-information/verification-validation-uncertainty).
For example, medical devices must comply with the [ASME V&V 40 standard](https://go.asme.org/vnv40committee) where reproducibility is part of the verification and validation process.
:::
