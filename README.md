# MuSus-100 Atlas

![cover](https://user-images.githubusercontent.com/22649869/185288716-5b80b58d-4f77-499a-bcfc-ddab0468004b.png)

Paper: https://assets.researchsquare.com/files/rs-994193/v1_covered.pdf

This is the official repository for the MuSus-100 QSM atlas. The repository includes multi-modal atlases in MNI space, along with the parcellation map of fine-grained deep brain nuclei and thalamus subregions. All files are in NIfTI format. 

If you find this work helpful in your research, please cite the original publication (preprint version) as follows. 

```
@article{he2021quantitative,
  title={Quantitative Susceptibility Atlas Construction in Montreal Neurological Institute Space: Towards Histological-consistent Iron-rich Deep Brain Nucleus Sub-region Identification},
  author={He, Chenyu and Guan, Xiaojun and Zhang, Weimin and Li, Jun and Liu, Chunlei and Wei, Hongjiang and Xu, Xiaojun and Zhang, Yuyao},
  year={2021}
}
```

## File structure
The `atlas` directory includes the MNI-spaced T1w, QSM, and hybrid atlases. The atlases are aligned to ICBM-152 2009c nonlinear atlas. 

The `label` directory includes the parcellation maps formatted in NIfTI, including the DBN (deep brain nuclei only), thalamus (thalamus subregions only), and the mixed (both deep brain nuclei and thalamus subregions). The corresponding label description is stored in the txt file formatted as the ITK-SNAP label description. 

## Usage
You may view the atlas and parcellation map by [ITK-SNAP](http://www.itksnap.org/) (or any other medical image viewer as you like). To view the atlas and label, open the atlas file in ITK-SNAP first and attach the label file as the `Segmentation` (you may directly drag the label file to the ITK-SNAP window showing an atlas and select `Load as Segmentation`). 

The label description files (txt files) can either be imported to ITK-SNAP or be directly viewed. 
To import a label description file into ITK-SNAP, click the `Segmentation` - `Import Label Descriptions...` and select the corresponding label file. You may load the segmentation first before you import the description file. 
To directly view a label description file, directly open the file with any text editor. The meaning of each column has been described in the file:

```
# Fields: 
#    IDX:   Zero-based index 
#    -R-:   Red color component (0..255)
#    -G-:   Green color component (0..255)
#    -B-:   Blue color component (0..255)
#    -A-:   Label transparency (0.00 .. 1.00)
#    VIS:   Label visibility (0 or 1)
#    IDX:   Label mesh visibility (0 or 1)
#  LABEL:   Label description 
```
