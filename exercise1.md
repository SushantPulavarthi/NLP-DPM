## Q1. State the primary contributions of this work. (2 Marks)

A1: The paper introduces an annotated dataset (10,637 paragraphs) to "identify and categorize language that is patronizing or condescending towards vulnerable communities". The goal being to be able to detect (and classify) more subtle harmful language, opposed to explicit harmful language. It also categorizes Patronizing and Condescending Language (PCL) into 3 high-level categories and 7 lower-level categories: "The Saviour" (unbalanced power relations, shallow solution), "The Expert" (presupposition, authority voice), and "The Poet" (metaphor, compassion, the poorer the merrier). They then also experiment with trying to detect and classify PCL, where they are able to get the best performance with BERT-based methods (mainly RoBERTa); which does well overall apart from classifying "metaphors" and "the poorer the merrier labels".

## Q2. Identify the technical strengths that justify the paper’s publication. (2 Marks)

They carefully consider the different scenarios for PCL in text, and have well-defined criterion and categories. The data is also sourced from the News on Web (NoW) corpus, and well-balanced data from 20 different countries and considering a wide range of texts.
Their method to using 2 annotators to annotate entire dataset and a referee; along with using Kappa Inter-Annotator Agreement also shows great care to avoid biases and other human errors within the dataset. With 3 levels that an annotator can report (0 - no PCL, 1 - borderline, 2 - contains PCL), which allows them to score the labelling to better identify positive & negative cases along with total disagreement cases (where 3rd annotator steps in).
Overall leading to a high-quality dataset where the labels are carefully considered and given proper PCL scores. By then testing and experimenting with this dataset (prediction of PCL and predicting category), they also provide a baseline metric and show that it is viable and showing room for future improvement.


## Q3. Highlight the key weaknesses or areas where the authors failed to provide sufficient evidence. (2 Marks)

They only have 2 annotators to go over classifying the entire dataset, therefore there is the potential that they may have similar biases and that it does not consider the view points from a multitude of people / communities or other issues like lack of knowledge / experience (may be harmful to a person from the community but not obvious to others). And where there was a total disagreement, although they come to a conclusion this is only done with 1 additional annotator.
Another issue is that out of the 10,637 paragraphs only 995 are positive PCL cases (9.354%). Which is not a high number, and may not be enough for models to fully learn and understand the subtleties of PCL. Also, although it is stated that the data is sourced from NoW corpus, there is not enough evidence on the range of types of media used. This data is sourced based on only 10 selected keywords (across 20 english speaking countries), which is limited and there is no evidence shown to whether the models are also able to consider other keywords that they did not pick out.

----

- had other category but did not use it

predicting presence of pcl (binary classification) and predicting the pcl category (multi-label classification)
BERT-based methods achieve highest results
10,637 paragraphs about potentially vulnerable groups
- only 10 keywords & paragraphs are roughly evenly split across each keyword and 20 english speaking countries (NoW - news on web corpus)
- only 995 are pcl
- 2 annotators to go over entire dataset and 1 referee

