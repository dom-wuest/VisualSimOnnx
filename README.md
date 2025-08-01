# Visual Similarity ONNX Model Conversion

CosPlace and EigenPlace are approches to create compact image descriptors. These are very useful for tasks like image retrieval and similarity search. The code by [Gabriele Berton](https://github.com/gmberton) provides a great starting point for working with these models. However it is not yet compatible with ONNX, which is a common format for deploying machine learning models. This document describes how to convert the CosPlace and EigenPlace model to ONNX format. Specifically, this enables export of dynamic axes such as batch size and image size, which is useful for inference in various applications.

This does require some modifications to the original code, but it is a straightforward process. The following steps outline how to achieve this conversion.

1. **Install Required Packages**: Make sure you have the necessary packages installed. You can do this via conda:
   ```bash
   conda env create -f environment.yml
   conda activate visual-sim-onnx
   ```
2. **Download some image for comparison**: You can use any image you like, I used images from the UAVid dataset. Place it in the root of the repository and name it `img.png` or change the code accordingly to use a different image.

3. **Open the Jupyter Notebook**: Open the Jupyter notebook `convert.ipynb` in your environment. This notebook contains the code for converting the model to ONNX format. All the steps are described in the notebook, including loading the model, preparing dummy inputs, and exporting the model.

## Acknowledgements
This work is based on the original code by [Gabriele Berton](https://github.com/gmberton). The original repository can be found at [CosPlace](https://github.com/gmberton/CosPlace) and [EigenPlace](https://github.com/gmberton/EigenPlaces). Check out his work!
