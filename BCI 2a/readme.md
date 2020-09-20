# AliK604's Fork of *multiscale-bci/IV-2a*

> Original title: Fast and Accurate Multiclass Inference for MI-BCIs Using Large Multiscale Temporal and Spectral Features. This is the code of an accepted conference paper submitted to EUSIPCO 2018. The preprint is available on this arXiv [link](https://arxiv.org/abs/1806.06823). If you are using this code please cite our paper. 

Data may be excluded. Get it from [the original repo](https://github.com/multiscale-bci/IV-2a/) and put in a folder classed `data_2a_mat` 

## Changes

I added more comments and added some ML models. Tested my ensemble of ML models with and without PCA. Without PCA (all data), I outperformed the authors’ Accuracy.

## Introduction 

>  [Dataset’s introduction paper](http://www.bbci.de/competition/iv/desc_2a.pdf)

​	As we humans think, we produce brain waves. These brain waves can be mapped to actual intentions. In this competition, you are given the brain wave data of people with the goal of spelling a word by only paying attention to visual stimuli. The goal of the competition is to detect errors during the spelling task, given the subject's brain waves. 

​	This data set consists of EEG data from 9 subjects. The cue-based BCI
paradigm consisted of four different motor imagery tasks, namely the imagination of movement of the left hand (class 1), right hand (class 2), both feet (class 3), and tongue (class 4). Two sessions on different days were recorded for each subject. Each session is comprised of 6 runs separated by short breaks. One run consists of 48 trials (12 for each of the four possible
classes), yielding a total of 288 trials per session

## Getting Started

First, download the source code.
Then, download the dataset "Four class motor imagery (001-2014)" of the [BCI competition IV-2a](http://bnci-horizon-2020.eu/database/data-sets). Put all files of the dataset (A01T.mat-A09E.mat) into a subfolder within the project called 'dataset' or change self.data_path in main_csp and main_riemannian. 

### Prerequisites

- python3
- numpy
- sklearn
- pyriemann
- scipy
- tensorflow 2.x 

The packages can be installed easily with conda and the _config.yml file: 
```bash
$ conda env create -f _config.yml -n msenv
$ source activate msenv 
```

### Recreate results

For the recreation of the CSP results run main_csp.py. 
Change self.svm_kernel for testing different kernels:
- self.svm_kernel='linear'  -> self.svm_c = 0.05
- self.svm_kernel='rbf'     -> self.svm_c = 20
- self.svm_kernel='poly'    -> self.svm_c = 0.1

```bash 
$ python3 main_csp.py
```
For the recreation of the Riemannian results run main_riemannian.py. 
Change self.svm_kernel for testing different kernels:
- self.svm_kernel='linear'  -> self.svm_c = 0.1
- self.svm_kernel='rbf'     -> self.svm_c = 20

Change self.riem_opt for testing different means:
- self.riem_opt = "Riemann"
- self.riem_opt = "Riemann_Euclid" 
- self.riem_opt = "Whitened_Euclid"
- self.riem_opt = "No_Adaptation"

```bash
$ python3 main_riemannian.py
```

## Authors
* **Michael Hersche** - *Initial work* - [MHersche](https://github.com/MHersche)
* **Tino Rellstab** - *Initial work* - [tinorellstab](https://github.com/tinorellstab)