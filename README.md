# File conversion tools for HDX

This repo is intended to house some tools for converting different HDX-MS software formats to the DynamX Cluster format for use in [Deuteros](https://github.com/andymlau/Deuteros_2.0).

### 1. HDExaminer   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/andymlau/File-conversion-for-HDX/blob/main/hdexaminer_convert.ipynb)
This tool converts the output of HDExaminer software to the DynamX Cluster format.



**Column mappings**

| New Column   | Existing Column | Calculation                              |
|--------------|-----------------|------------------------------------------|
| Protein      | Protein         |                                          |
| Start        | Start           |                                          |
| End          | End             |                                          |
| Sequence     | Sequence        |                                          |
| Modification |                 | Leave empty                              |
| Fragment     |                 | Leave empty                              |
| MaxUptake    |                 | Calculate from sequence: (n_res-n_pro-1) |
| MHP          |                 | 'Exp Cent' - '# Deut'                    |
| State        | Protein State   |                                          |
| Exposure     | Deut Time       | Remove trailing 's'                      |
| File         | Experiment      |                                          |
| z            | Charge          |                                          |
| RT           | Search RT       |                                          |
| Inten        | Max Inty        |                                          |
| Center       | Exp Cent        |                                          |
