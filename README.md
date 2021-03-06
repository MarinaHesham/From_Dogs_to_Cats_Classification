# From Dogs to Cats Breeds Classification
This repository is created to explore transfer learning strategies by training a model to classify images of dogs and then fine tune it to classify a dataset of cats breeds.

## Requirements
- Install pytorch `pip3 install torch torchvision`
- Get a [kaggle api token](https://www.kaggle.com/docs/api): My Account --> scroll down to Create New API token.
- Place `kaggle.json` in `~/.kaggle` directory. (If `~/.kaggle` directory does not exist, create one first).

## Download Datasets
In our experiments, we use these two datasets: 
1. [Stanford Dogs Dataset](https://www.kaggle.com/jessicali9530/stanford-dogs-dataset)
2. [Cat Breeds Dataset](https://www.kaggle.com/ma7555/cat-breeds-dataset#cats.csv)

To download these datasets, execute this command
```
python download_datasets.py
```

## Training a ResNet18 Model
Train a ResNet18 model on the dogs dataset.

```
python train.py --dataset_name dogs
```
We have two dataset options to train: `dogs` and `cats`.

## Fine-Tuning on Cats Dataset
Fine-tune the pretrained model on the cats dataset

```
python fine_tune.py --pretrained-model dogs
```
We have two options for pretrained model: `dogs` and `imagenet`. 


### Note:
This work is done as the final project for CS1430 Computer Vision class.

### Team Members:
- Albert Webson (albert_webson@brown.edu)
- Nihal Vivekanand Nayak (nihal_vivekanand_nayak@brown.edu)
- Marina Neseem (marina_neseem@brown.edu)
