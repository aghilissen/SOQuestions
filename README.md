# Understanding what constitutes a great Stack Overflow questions (or classification of 60,000 questions from Stack Overflow)

# The Dataset
The dataset is [sourced from Kaggle](https://www.kaggle.com/imoore/60k-stack-overflow-questions-with-quality-rate).

I find it interesting for a few reasons:
* This dataset is quite neat: 6 columns, 60,000 observations, no missing values, and, as far as text data goes, it is rather structured.
* It is well defined. The questions are from [Stack Overflow](https://stackoverflow.com/) and were posted between 2016 and 2020. The topics are all programming related.
* It is made of text data but there are a few levels to play with: `Tag` analysis, `Title` and `Body` analysis, correlate those with quality and/or time.
* At the time I discovered it, it only had a couple of notebooks. I didn't manage to spend as much time as I wanted on this project but it is always tempting to have a peak when notebooks are available, so I'll try to stay away from them :)

# The Repository Structure
| File | Description |
| --- | --- |
| [Data  folder](./data/) | Contains 2 folders: `raw`, the source data, and `processed`. After the EDA, the text has been cleaned and this `data.csv` is the one used in the subsequent analysis. |
| [Image folder](./img) | Folder containing images: Some graphs but also random pictures used in blog posts |
| [EDA](./01-EDA.ipynb) | Exploratory Data Analysis, resulting in the processed data |
| [Tag Analysis](./02-TagAnalysis.ipynb) | Analysis of the question tags. There is no prediction/classification at this point, I still consider this as part of the EDA. | 
| [Word Analysis](./03-WordAnalysis.ipynb) | Analysis of the `Body` column. There is no prediction/classification at this point, I still consider this as part of the EDA. |

# Insights
## From the Tags field
* Javascript is the most popular programming language on SO, followed by Python, then Java and C#.
  * Javascript is frequently associated with jquery, html and css and the community is clearly using JS for web development (if we had any doubts).
  * Python is associated with pandas, regex, lists, and dictionaries. The community is definitely into data science, and seem to be relatively new to the subject (as python basics such as lists and dictionaries are quite up this list). But web dev and dev are also part of the show with questions about django and tkinter.
  * The Java community is mainly concerned about Android and Java-8 development.
* There is no clear correlation between the quality of a post and the tags used. However, We can see some variations depending on the programming language:
  * Python is very close to parity on question quality, with a slight excess in `LQ_CLOSE` questions(HQ:LQ_EDIT:LQ_CLOSE is 1:1.1:1.2).
  * As opposed to Java which seems to be skewed towards low-quality questions (1:2.2:2.6).

_Work by [Antoine Ghilissen](https://github.com/aghilissen)_