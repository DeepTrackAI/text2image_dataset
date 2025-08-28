# Text-to-Image Transformed MNIST Dataset (text2image_dataset)

## Overview

This DeepTrackAI repository contains a dataset of transformed MNIST digits paired with natural-language descriptions.  
Images are generated using the notebook [create_transformed_images.ipynb](https://github.com/DeepTrackAI/text2image_dataset/blob/main/create_transformed_images.ipynb), which applies randomized color, rotation/flip, and contrast transformations to the original MNIST digits and saves both the transformed images and corresponding text prompts.

The dataset is designed for benchmarking text-to-image alignment and multimodal learning tasks.

### Summary
- **Dataset Size**: equal to the number of [MNIST](http://yann.lecun.com/exdb/mnist/) images (60,000), each with one transformed version  
- **Image Size**: 28 × 28 pixels  
- **Format**: 8-bit RGB PNG images  
- **Metadata**: JSON file mapping filenames to natural-language transformation descriptions  
- **Transformations included**:  
  - Digit colorization (e.g. “in red on a blue background”)  
  - Rotations (±90°, 180°)  
  - Horizontal mirror / vertical flip  
  - Auto-contrast normalization  

---

## Original Source

- **Title**: The MNIST Database of Handwritten Digits  
- **Authors**: Yann LeCun, Corinna Cortes, Christopher J.C. Burges
- **Source**: [Official MNIST Website](http://yann.lecun.com/exdb/mnist/)  
- **License**: [Creative Commons Attribution-Share Alike 3.0](https://creativecommons.org/licenses/by-sa/3.0/)

The transformed dataset in this repository is based on MNIST and therefore distributed under the same license. If you use this dataset, please follow the licensing requirements and provide proper attribution to the original authors.

---

## Dataset Structure

```bash
/text2image_dataset  
  └── train/  
      ├── images/  
      │   ├── 0_00001.png  
      │   ├── 0_00002.png  
      │   └── ...  
      └── image_descriptions.json  
```

- `images/` contains transformed digit images in PNG format.  
- `image_descriptions.json` stores a dictionary mapping filenames to textual descriptions of the transformations.

---

## How to Access the Data

### Clone the Repository
```bash
git clone https://github.com/DeepTrackAI/text2image_dataset  
cd text2image_dataset  
```

### Generate the Dataset
Run the notebook to generate transformed images and their descriptions:
```bash
jupyter notebook create_transformed_images.ipynb
```
---

## Attribution

When using this dataset or the code, please cite both the original MNIST dataset and the text-to-image transformation repository.

### Cite MNIST:
LeCun Y, Cortes C, Burges CJC. *The MNIST Database of Handwritten Digits.* 
Retrieved from [http://yann.lecun.com/exdb/mnist/](http://yann.lecun.com/exdb/mnist/)

```bibtex
@misc{lecun1998mnist,
  title        = {The MNIST Database of Handwritten Digits},
  author       = {LeCun, Yann and Cortes, Corinna and Burges, Christopher J.C.},
  year         = {1998},
  howpublished = {\url{http://yann.lecun.com/exdb/mnist/}}
}
```

### Cite this repository:
Carlo Manzo. *Text-to-Image Transformed MNIST Dataset*. GitHub (2025).  
[GitHub](https://github.com/DeepTrackAI/text2image_dataset)

```bibtex
@misc{text2image2025,  
  author       = {Carlo Manzo},  
  title        = {Text-to-Image Transformed MNIST Dataset},  
  year         = {2025},  
  howpublished = {\url{https://github.com/DeepTrackAI/text2image_dataset}}  
}  
```

---

## License

This dataset is shared under the **Creative Commons Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0)** License, following the original licensing terms.
