requirements.txt		environment requirements
utils.py			utilities
evaluate_model.py		evaluate models using test data
models.py		models for Causal-STGAT
train.py			train the model
data
 —trajectories.py		read files and build dataloder for the trajectory datasets
 —loader.py		return pytorch dataset and loader


This code is based on STGAT: https://github.com/huang-xx/STGAT
Reference:
    Huang Y, Bi H K, Li Z, et al. STGAT: Modeling Spatial-Temporal Interactions for Human Trajectory Prediction,ICCV19.


how to train the model
1. Download datasets from: https://github.com/abduallahmohamed/Social-STGCNN/tree/master/datasets to causal_stgat_code/datasets
directories are like: causal_stgat_code/datasets/univ, causal_stgat_code/datasets/eth

2. To set up the environment run:
pip install -r requirements.txt

3. To train run:
python train.py --dataset_name "eth"

4. To test run
python evaluate_model.py --dataset_name "eth" --resume "your_checkpoint.pth.tar"