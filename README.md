# binGAN

This code implement the binGAN method, that was presented in 
*Zieba M., Semberecki P. El-Gaaly T., Trzcinski T.. "BinGAN: Learning Compact Binary Descriptors with a Regularized GAN."* [arxiv](https://arxiv.org/pdf/1806.06778.pdf) 

The training code requires [Lasagne](http://lasagne.readthedocs.io/en/latest/). Using GPU is highly advised.

## Running the code

The procedure of training binGan is run with `train_model.py` script. 

There are two datasets for two tasks in which binGAN is evaluated:
- Brown dataset (image matching)
- Cifar10 (image retrieval)    

Selecting the proper dataset is performed in `settings.py`, by setting proper value of `dataset_type` parameter. In this file it is possible also to set various type of training hyperparameters described in details in the [paper](https://arxiv.org/pdf/1806.06778.pdf).

Brown dataset, which is composed of three subsets: `yosemite`, `notredame` and `liberty`. It is crucial to specify, which training and validation set by setting proper values to parameters: `data_name` and `test_data`. 

It is crucial to set proper value of binary features (`num_features`), while switching between datasets.

The quality of image matching on Brown dataset is evaluated by script `test_brown.py`

The quality of image retrieval on Cifar10 dataset is evaluated by script `test_cifar10.py` 


  