# Focal-Unet: Unet-like Focal Modulation for Medical Image Segmentation


[![arXiv](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2212.09263)
[![GitHub Stars](https://img.shields.io/github/stars/givkashi/Focal-Unet?style=social)](https://github.com/givkashi/Focal-Unet)
![visitors](https://visitor-badge.glitch.me/badge?page_id=givkashi/Focal-Unet)

<br>

[[Project page](https://givkashi.github.io/focal-unet/)]

<details>
    <summary>Abstract (click to view)</summary>
	Recently, many attempts have been made to construct a transformer base U-shaped architecture, and new methods have been proposed that outperformed CNN’s base rivals. However, serious problems such as blockiness and cropped edges in predicted masks remain because of transformers’ patch partitioning operations. In this work, we propose a new U-shaped architecture for medical image segmentation with the help of the newly introduced focal modulation mechanism. The proposed architecture has asymmetric depths for the encoder and decoder. Due to the ability of the focal module to aggregate local and global features, our model could simultaneously benefit the wide receptive field of transformers and local viewing of CNNs. This helps the proposed method balance local and global feature usage to outperform one of the most powerful transformer-based U-shaped models, Swin-UNet. We achieved a 1.68% higher DICE score and a 0.89 better HD metric on the Synapse dataset. Also, with extremely limited data, we had a 4.25% higher DICE score on the NeoPolyp dataset. 
</details>
<br>
<div  align="center">
    <img src="./figs/fig1.png" width="90%">
</div>
<p align="center" "font-size:14px;">
Overview of the Focal-UNet architucture
</p>

---

## Our Results
<br>
<div  align="center">
    <img src="./figs/fig2.png" width="90%">
</div>
<p align="center" "font-size:14px;">
The segmentation results of Swin-UNet and Focal-UNet on Synapse dataset
</p>

<br>

<div  align="center">
    <img src="./figs/fig3.PNG" width="80%">
</div>
<p align="center" "font-size:14px;">
The segmentation results of Swin-UNet and Focal-UNet on NeoPolyp dataset
</p>
<br>

---

##  Environment

- Use the command "pip install -r requirements.txt" for install dependencies.
<br>

## Prepare data

- Synapse dataset: Please go to ["./datasets/README.md"](datasets/README.md) for details, or send an Email to givkashi AT gmail.com to request the preprocessed data.

- NeoPolyp dataset: Please go to [Kaggle](https://www.kaggle.com/c/bkai-igh-neopolyp/) for download this dataset.

<br>

## Download pre-trained model 

- The pre-trained model on Synapse dataset is available at: [google drive](https://drive.google.com/drive/folders/1tq8-p4XXg-0mbbciqoN911Hd__PSWQEc?usp=sharing).

- The pre-trained model on NeoPolyp dataset will be available.

<br>

## Test

- Put the pre-trained model in `./checkpoint`.

- Run

```bash
python test.py
```
<br>

## Train

- Download pre-trained focalnet tiny lrf from [here](https://drive.google.com/drive/folders/13SecOXT1cSAZpvzgkZ36ug9giwg9VRHb?usp=sharing). Put it in `./pretrained_focal` folder.

- Put Synapse dataset in `./data/Synapse`.

- Run train.py on synapse dataset.

```bash
python train.py
```

<br>

## Acknowledgments


* [Focal Modulation Networks](https://github.com/microsoft/FocalNet)
* [Swin-Unet](https://github.com/HuCaoFighting/Swin-Unet)

<br>

## Citation
If you found this code helpful, please consider citing: 
```
@article{naderi2022focal,
  title={Focal-UNet: UNet-like Focal Modulation for Medical Image Segmentation},
  author={Naderi, MohammadReza and Givkashi, MohammadHossein and Piri, Fatemeh and Karimi, Nader and Samavi, Shadrokh},
  journal={arXiv preprint arXiv:2212.09263},
  year={2022}
}
```
