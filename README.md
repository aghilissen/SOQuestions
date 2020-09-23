# Understanding what constitutes a great Stack Overflow questions (or classification of 60,000 questions from Stack Overflow)

# The Dataset
The dataset is [sourced from Kaggle](https://www.kaggle.com/imoore/60k-stack-overflow-questions-with-quality-rate).

I find it interesting for a few reasons:
* This dataset is quite neat: 6 columns, 60,000 observations, no missing value and, as far as text data goes, it is rather structured.
* It is well defined. The questions are from [Stack Overflow](https://stackoverflow.com/) and were posted between 2016 and 2020. The topics are all programming related.
* It is made of text data but there are a few level to play with: `Tag` analysis, `Title` and `Body` analysis, correlate those with quality and/or time.
* At the time I discovered it, it only had a couple of notebooks. I didn't manage to spend as much time as I wanted on this project but it is always tempting to have a peak when notebooks are available, so I'll try to stay away from them :)

# The Repository Structure:
| File | Description |
| --- | --- |
| [Data  folder](./data/) | Contains 2 folders: `raw`, the source data, and `processed`. After the EDA, the text has been cleaned and this `data.csv` is the one used in the subsequent analysis. |
| [Image folder](./img) | Folder containing images: Some graphs but also random pictures used in blog posts |
| [01-EDA](./01-EDA.ipynb) | Exploratory Data Analysis, resulting in the processed data |

_Work by [Antoine Ghilissen](https://github.com/aghilissen)_