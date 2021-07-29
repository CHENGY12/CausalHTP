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


## Dataset

The datasets can be found in `datasets/`, we provide 5 scenes including eth, hotel, univ, zara1, and zara2.

## Training and Evaluation

You can train the model for eth dataset as 
```
python train.py --dataset_name "eth"
```

To evaluate the trained model, you can use
```
python evaluate_model.py --dataset_name "eth" --resume "your_checkpoint.pth.tar"
```
The pre-trained models can be found in `pretrain/`

## Result

| Results (ADE/FDE) | ETH   | HOTEL | ZARA1 | ZARA2 | UNIV | AVG |
| :------------: | :---: | :---: | :---: | :---: | :---: | :---: |
| STGAT          | 0.73/1.39 | 0.38/0.72 | 0.35/0.69 | 0.32/0.64 | 0.57/1.22 | 0.47/0.93 |
| Causal-STGAT   | 0.60/0.98 | 0.30/0.54 | 0.32/0.64 | 0.28/0.58 | 0.52/1.10 | 0.40/0.77 |

## Citation

Please use the citation provided below if it is useful to your research:

```
@inproceedings{CausalHTP,
  title={Human Trajectory Prediction via Counterfactual Analysis},
  author={Chen, Guangyi and Li, Junlong and Lu, Jiwen and Zhou, Jie},
  booktitle={ICCV},
  year={2021}
}
```