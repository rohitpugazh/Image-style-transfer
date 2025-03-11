# Image Style Transfer

## Overview

This project demonstrates how the feature representations learned by high-performing Convolutional Neural Networks (CNNs) can be utilized to independently process and manipulate the content and style of natural images. The proposed algorithm constrains a texture synthesis method using feature representations from state-of-the-art CNNs, enabling the creation of new images that combine the content of one image with the style of another.

## Features

- **Content and Style Separation**: Utilizes CNNs to extract and recombine content and style from different images.
- **Texture Synthesis**: Employs advanced texture synthesis techniques guided by CNN feature representations.
- **Flexible Image Generation**: Allows users to generate images that blend the content of one image with the artistic style of another.

## Installation & Setup

### Prerequisites

- **Python 3.7+**: Ensure you have Python installed. You can download it from the [official Python website](https://www.python.org/).
- **PyTorch**: The project relies on PyTorch for neural network operations. Installation instructions can be found on the [PyTorch website](https://pytorch.org/get-started/locally/).

### Steps to Set Up the Project

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/rohitpugazh/Image-style-transfer.git
   cd Image-style-transfer
   ```

2. **Set Up a Virtual Environment** (Optional but recommended):

   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   ```

3. **Install Required Packages**:

   ```bash
   pip install -r requirements.txt
   ```

   If `requirements.txt` is not provided, manually install the dependencies:

   ```bash
   pip install torch torchvision matplotlib numpy pillow requests
   ```

## Usage

### Running Style Transfer

To perform style transfer, modify and run `style_transfer.py` as follows:

```python
from style_transfer import run_style_transfer

content_path = "images/content.jpg"
style_path = "images/style.jpg"
output_path = "results/output.jpg"

run_style_transfer(content_path, style_path, output_path, num_steps=2000, style_weight=1e6, content_weight=1)
```

### Parameters

- `content_path`: Path to the content image file.
- `style_path`: Path to the style image file.
- `output_path`: Path to save the generated output image.
- `num_steps`: Number of optimization steps (default: 2000).
- `style_weight`: Weight for style reconstruction (default: 1e6).
- `content_weight`: Weight for content reconstruction (default: 1).

## File Structure

```
Image-style-transfer/
│── images/                # Directory containing input images
│── results/               # Directory to save output images
│── LICENSE                # License file
│── README.md              # Project documentation
│── style_transfer.py      # Main script for style transfer
│── requirements.txt       # Python dependencies
```

## Dependencies

- **Python Packages**:
  - `torch`: PyTorch for neural network operations.
  - `torchvision`: For image handling and transformations.
  - `matplotlib`: For visualization.
  - `numpy`: For numerical computations.
  - `pillow`: For image processing.
  - `requests`: For handling image URLs.

  Install all dependencies using:

  ```bash
  pip install -r requirements.txt
  ```

## License

This project is licensed under the GNU General Public License v3.0. See the `LICENSE` file for more details.

## Acknowledgments

- **Gatys et al.**: The foundational work on neural style transfer that inspired this project.
- **PyTorch Community**: For providing tools and resources that facilitated the development of this project.

For any questions or issues, please open an issue on GitHub or contact the repository owner.

