# nba-neuralnetwork-prediction
My approach for nba games predictions using dnn and cnn with custom dataset
# Dataset
I created my own dataset for this problem. I chose last 6 years of nba games history. For every game we want to predict, I created json file with weighted average of last 10 games for two teams that we are trying to predict. With that in mind I created 4 different variations of dataset.
  - basic/advance statistics treating team as one unit
  - basic/advance statistics treating team as 7 players where last player is a combinations of roleplayers

Moving forward I am going to refer to them as bst,bsp,ast,asp.\n
It is important to know that datasets are not balanced because of the way i scrapped the data. 57.62% of games are won by home teams and i labaled all home team wins as 1. I could fix that but I was wondering if this will help my networks with phenomenon called home court advantage.
# Neural networks
I created 8 different but simmilar networks. I wanted to see better how my datasets affect my learning and choose best data for future experiments.
Have in mind it is my first attempt in this field and I hope first of many. I used tensorflow.keras as my starting point. 
# Results

For now I selected validation accuracy that in my opinion best represents current state of models. 

Dnn | bst | bsm | ast | asp 
--- | --- | --- | --- |---
Accuracy | 0.6389 | 0.6246 | 0.6213 | 0.6451 

Cnn1d | bst | bsm | ast | asp 
--- | --- | --- | --- |---
Accuracy | 0.6289 | 0.6110 | 0.6312 | 0.6528 
