# Text-to-Image Transformed MNIST Dataset (text2image_dataset)

## Overview

This DeepTrackAI repository contains a dataset of transformed MNIST digits paired with natural-language descriptions.  
Images are generated using the notebook [create_transformed_images.ipynb](https://github.com/DeepTrackAI/text2image_dataset/blob/main/create_transformed_images.ipynb), which applies randomized color, rotation/flip, and contrast transformations to the original [MNIST](http://yann.lecun.com/exdb/mnist/) digits and saves both the transformed images and corresponding text prompts.

The dataset is designed for benchmarking text-to-image alignment and multimodal learning tasks.

### Summary
- **Number of images**: equal to the number of MNIST images (60,000), each with one transformed version
- **Image size**: 28 × 28 pixels  
- **Image format**: 8-bit RGB PNG 
- **Metadata**: JSON file mapping filenames to natural-language transformation descriptions  
- **Transformations included**:  
  - Digit colorization (e.g., “in red on a blue background”)  
  - Rotations (±90°, 180°)  
  - Horizontal mirror / vertical flip  
  - Auto-contrast normalization  

---

## Original Source

- **Base dataset**
 - **Title**: The MNIST Database of Handwritten Digits  
- **Authors**: Yann LeCun, Corinna Cortes, Christopher J.C. Burges  
- **Source**: [Official MNIST Website](http://yann.lecun.com/exdb/mnist/)
- **Reference article**: LeCun, Y., Bottou, L., Bengio, Y., & Haffner, P. *Proceedings of the IEEE* 86(11): 2278-2324 (1998). [DOI: 10.1109/5.726791](https://doi.org/10.1109/5.726791) 
- **License**: [Creative Commons Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0)](https://creativecommons.org/licenses/by-sa/3.0/)
- **Note**: The original MNIST website is no longer actively maintained. An [archived version](https://web.archive.org/web/20200430193701/http://yann.lecun.com/exdb/mnist/) is available, and the dataset is widely mirrored (e.g., on Kaggle)./)

- **Derivative dataset**
  - **Title**: Text-to-Image Transformed MNIST Dataset  
  - **Authors**: Carlo Manzo  
  - **Source**: This repository
  - **License**: [Creative Commons Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0)](https://creativecommons.org/licenses/by-sa/3.0/)
  
If you use this dataset in your research, please follow the licensing requirements and properly attribute the original authors.

---

## Dataset Structure

```bash
/text2image_dataset  
└── train/  
    ├── images/                 # Transformed digit images 
    │   ├── 0_000000.png  
    │   ├── 0_000001.png  
    │   └── ...  
    └── image_descriptions.json # Mapping of filenames to natural-language transformation descriptions  

```

Each filename in`images/` begins with the digit label (0–9), followed by a sequential numerical identifier.
The JSON file provides the corresponding text description for each transformed image.

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

When using this dataset or the code, please cite the original MNIST dataset, the reference article, and the text-to-image transformation repository.

### Cite the dataset:
LeCun Y, Cortes C, Burges CJC. *The MNIST Database of Handwritten Digits.* Retrieved from [http://yann.lecun.com/exdb/mnist/](http://yann.lecun.com/exdb/mnist/)

```bibtex
@misc{lecun1998mnist,
  title        = {The MNIST Database of Handwritten Digits},
  author       = {LeCun, Yann and Cortes, Corinna and Burges, Christopher J.C.},
  year         = {1998},
  howpublished = {\url{http://yann.lecun.com/exdb/mnist/}}
}
```

### Cite the reference article:
LeCun Y, Bottou L, Bengio Y, Haffner P. *Gradient-based learning applied to document recognition.* Proceedings of the IEEE, 86(11): 2278–2324 (1998). [DOI: 10.1109/5.726791](https://doi.org/10.1109/5.726791)

```bibtex
@article{lecun1998gradient,
  title     = {Gradient-based learning applied to document recognition},
  author    = {LeCun, Yann and Bottou, L{\'e}on and Bengio, Yoshua and Haffner, Patrick},
  journal   = {Proceedings of the IEEE},
  volume    = {86},
  number    = {11},
  pages     = {2278--2324},
  year      = {1998},
  publisher = {IEEE},
  doi       = {10.1109/5.726791}
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

This dataset is shared under the [Creative Commons Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0)](https://creativecommons.org/licenses/by-sa/3.0/) License, following the original licensing terms.



