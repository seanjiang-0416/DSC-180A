# Unraveling Truths: An Exploration of Fact Checking through Diverse Factuality Factors

The project mainly focus on creating a fact-checking system by including factuality factors like credibility, context veracity, and political affiliation. The project outcome consists of two parts. The first part is built based on data collected from Politifact, which experiment on using all three factuality factors. The second part is built based on data from the Liar-Liar-Plus dataset, which utilizes only credibiliity and political affiliation, but we included other features such as sentiment analysis on justifications and text embeddings on the statements.


## Retrieving the data locally
(1) Preprocessed data stored in data file locally
(2) Politifact.com raw data stored at: https://drive.google.com/file/d/1hHS3oUW7H1KdC341LeYAsroaJiWWcnL7
(3) Liar Liar Plus dataset from https://github.com/Tariq60/LIAR-PLUS
(4) Contexual Shift Preprocessed data: https://drive.google.com/file/d/16ohLi5nbC0yYk6oNou8YArLQY2cxnQWm
(5) Political affiliation dataset from: https://www.kaggle.com/datasets/kapastor/democratvsrepublicantweets

## Running the project

To install the dependencies, run the following command from the root directory of the project: pip install -r requirements.txt

To fetch repo to local machine, please run git clone https://github.com/seanjiang-0416/DSC-180A.git on the terminal

To get result for the first part of the project:
    Restart and run all cells in src/stacked_model.ipynb, output would be recorded at the end of the notebook
    This notebook includes a combination of three factors -- credibility, political affiliation, and context veracity. Each step can be refered to its experimental notebook located in the notebook file from the root. The output contains a GridSearchCV and the best accuracy model and its parameters.

To get result for the second part of the project:
    Restart and run all cells in src/liar_model.ipynb, output would be recorded at the end of the notebook
    This notebook is a hackathon on the Liar-Liar-Plus dataset. It combines some factors like credibility and political affiliation. It also did distillation by using pre-trained sentiment-scoring model to score the justification text and used as another factor in the model. The final model also included a Bert text-embedding of the statements which got truncated to the first 50 to lower its weight. The output contains a GridSearchCV and the best accuracy model and its parameters. 