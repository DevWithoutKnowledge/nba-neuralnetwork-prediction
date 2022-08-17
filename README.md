# nba-neuralnetwork-prediction
My approach for nba games predictions using dnn and cnn with custom dataset
# Dataset
I created my own dataset for this problem. I chose last 6 years of nba games history. For every game we want to predict, I created json file with weighted average of last 10 games for two teams that we are trying to predict. With that in mind I created 4 different variations of dataset.
- basic/advance statistics treating team as one unit
- basic/advance statistics treating team as 7 players where last player is a combinations of roleplayers
Moving forward I am going to refer to them as bst,bsp,ast,asp.
# Results
Cnn1d | bst | bsm | ast | asp 
--- | --- | --- | --- |---
Accuracy | 301 | 283 | 290 | 286 
