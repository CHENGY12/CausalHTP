# Human Trajectory Prediction via Counterfactual Analysis (CausalHTP)
The official PyTorch code implementation of "Human Trajectory Prediction via Counterfactual Analysis" in ICCV 2021.

## News
We add the implementation of our project Causal-STGAT, where we apply our CausalHTP method to the baseline backbone network [STGAT](https://github.com/huang-xx/STGAT). The code of Causal-STGCNN is coming soon.

## Introduction

Most trajectory prediction methods concentrate on modeling the environment interactions and aggregate these interaction clues
with history behavior clues for trajectory prediction. However, there are heavy biases in the between training and deployment environment interactions. The motivation of this project is to mitigate the negative effects of the inherent biases. We propose a
counterfactual analysis method to alleviate the overdependence of environment bias and highlight the trajectory clues itself. This counterfactual analysis method is a plug-and-play module which can be easily applied to any baseline predictor, and consistently improves the performance on many human trajectory prediction benchmarks.


## Requirements
- Python 3.6+
- PyTorch 1.3

To build all the dependency, you can follow the instruction below.
```
pip install -r requirements.txt
```



 provide the requirement 


please follow the instruction below.

