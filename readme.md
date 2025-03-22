# Self-Presentation in Rap Lyrics - PSL Week NLP for Social Sciences (October 2024)

## Project Overview
This project was conducted as part of PSL Week NLP for Social Sciences (October 2024). The methodology was introduced by Mr. Christophe Benevent at the beginning of the week and was previously applied to analyze Airbnb hosts. The dataset is based on the work of [Benoit de Courson](lien_vers_le_travail_de_benoit_de_courson).

## Acknowledgments
We thank Mr. Christophe Benevent for his guidance https://github.com/BenaventC/RapFrance/blob/main/README.md and Benoit de Courson  https://huggingface.co/datasets/regicid/LRFAF for providing the dataset that made this analysis possible.

## Methodology
To study self-presentation, lyrics containing the pronouns **je, j’, moi, m’,** and **me**, along with the following lines, were extracted. Fifty labels were selected based on their relevance after an initial review of the lyrics. These labels include:

- **Self-made man**
- **Success**
- **Merit**
- **Hard work**
- **Inspiring**
- **Ambitious**
- **Individualism**
- And others

A zero-shot classification was then performed, computing a score between **0 and 1** to indicate how well each label fits the hypothesis template: *“The author of these lyrics could be described as […]”*.

## Analysis and Refinement
Upon reviewing the results, some labels were deemed irrelevant, as their scores were consistently close to zero across all songs. These labels were removed, and a **covariance matrix** was constructed to analyze correlations between the remaining labels. 

Two strongly correlated groups emerged:
1. **Revolt, relentless, avant-garde**
2. **Artist, music, self-made man**

This suggests two possible axes of analysis.

## Clustering and PCA
Principal Component Analysis (**PCA**) was performed, followed by clustering. Using the **elbow method** to determine the optimal number of clusters, the raps were classified into **four distinct groups**, each representing a different form of self-presentation:

- **Cluster 0:** Strong scores in **antihéros** and **critique**, suggesting a self-image centered around defiance and opposition.
- **Cluster 1:** High scores in **provocateur** and **insolent**, with notable scores in **antihéros** and **critique**, indicating a persona blending rebellion with ambition.
- **Cluster 2:** Defined by **passion, révolte, provocateur,** and **porte-voix**, reflecting a more engaged and vocal self-presentation, often associated with activism or advocacy.
- **Cluster 3:** High scores in **artiste, musician,** and **créateur**, representing rappers who emphasize their artistic and musical identity over political or rebellious themes.

![Cluster 0](image.png)  
*Cluster 0*

![alt text](image-1.png)
*Cluster 1*

![alt text](image-2.png)
*Cluster 2*

![alt text](image-3.png)
*Cluster 3*

