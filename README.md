# Automatic renal carcinoma biopsy guidance using forward-viewing endoscopic optical coherence tomography and deep learning

Code for the accepted paper in Communications Engineering.
The paper can be found in this link: https://www.nature.com/articles/s44172-024-00254-9

## Dataset
The dataset is on Zenodo: https://zenodo.org/records/12170637, more kidneys will pe provided in the future.

## Stages of training:
1. 5-fold cross-validaiton for CNN architectures and hyperparameters selection. InceptionV3 and ResNet50 were chosen.
2. Cross-testing without validation set to benchmark the model performance on the test set.
3. Trained the model with all five subjects. Testing of the model's prediciton on 5 additional hold-out test-sets to prove the generalizaion capability of the model.

## Usage:
1. Configuring your json file under the path of /scripts/training/training_config_file/
2. Under the path of /scripts, run the following command: ```python3 -m training.training_sequential.loop_outer.training_outer_loop --config_file ./training/training_config_files/loop_outer/your_json_file```




