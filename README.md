# MIMSTransUNet
This repo holds code for MIMSTransUNet: Mulit Image Modality Segmentor using TransUNet

## Usage

### 1. Test the model
You can find instructions on the how to test the architechure using the synapse multi-organ [dataset](https://drive.google.com/drive/folders/1ACJEoTp-uqfFJ73qS3eUObQh52nGuzCd?usp=sharing) at [TransUNet](https://github.com/Beckschen/TransUNet)
### 2. Prepare data

Please go to ["./datasets/README.md"](datasets/README.md) for details.

### 3. Environment

Please prepare an environment with python=3.7, and then use the command "pip install -r requirements.txt" for the dependencies.

### 4. Train/Test

- Run the train script on synapse dataset. 

```bash
python train.py --dataset Synapse --vit_name R50-ViT-B_16 --batch_size=6 --base_lr=0.01 --max_epochs=150 --max_iterations=30000
```

- Run the test script on synapse dataset. It supports testing for both 2D images and 3D volumes. --is_savenii flag saves the predcitions with appropariate spacing from nifiti image metadata.

```bash
python test.py --dataset Synapse --vit_name R50-ViT-B_16 --is_savenii
```

## Reference
* [TransUNet](https://github.com/Beckschen/TransUNet)

## Citations

```bibtex
@article{

}
```
