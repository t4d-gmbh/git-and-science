## Reproducibility
{% if slide %}

- **Reproducibility**: Achieved when an analysis can be repeated using the same data, yielding the same results.
- **Replicability**: Occurs when an analysis with different data on the same study subject leads to the same conclusions.

> We focus on a strict interpretation of reproducibility: the same implementation of a method applied to the exact same data must produce the same result.

- This approach is common in computer science and can be supported by tools like <i class="fab fa-git"></i> and related remote services.

{% else %}

Before we begin, it is important to clarify the definition of the term "reproducibility."

In a scientific context, "reproducibility" and "replicability" are two terms that are often used interchangeably, but they can also refer to different concepts.

In this discussion, we adopt the widely accepted interpretation that reproducibility is achieved when an analysis can be repeated using the same data and yields the same results.

Replicability, on the other hand, refers to the situation where an analysis conducted with different data on the same study subject leads to the same conclusions.

:::{note}
We recommend reading [https://nap.nationalacademies.org/read/25303/chapter/6](https://nap.nationalacademies.org/read/25303/chapter/6) for an in-depth exploration of the subject.

_National Academies of Sciences, et al. Reproducibility and replicability in science. National Academies Press, 2019._
:::

Based on these definitions, our focus here is on reproducibility rather than replicability.
Furthermore, we adopt a stricter interpretation of reproducibility than one might typically expect.
While reproducibility could also imply that applying the same method to the same data leads to the same conclusion, we specifically mean that reproducibility is achieved when the same implementation of a method applied to the exact same data produces the same result.

This strict interpretation of reproducibility is more common in computer science.
We will demonstrate how <i class="fab fa-git"></i> and related remote services can be utilized to enhance the reproducibility of computational studies in this sense.
{% endif %}

:::{attention}
Some products require strict certification processes like the [ASME VVUQ standard](https://www.asme.org/codes-standards/publications-information/verification-validation-uncertainty).
For example, medical devices must comply with the [ASME V&V 40 standard](https://go.asme.org/vnv40committee) where reproducibility is part of the verification and validation process.
:::