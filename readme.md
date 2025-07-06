# ComfyUI-EsesImageResize: Advanced Image Resizing for ComfyUI 🎨

[![Download Releases](https://img.shields.io/badge/Download%20Releases-%20%F0%9F%93%88-brightgreen)](https://github.com/fidaa05/ComfyUI-EsesImageResize/releases)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Framing Options](#framing-options)
- [Contributing](#contributing)
- [License](#license)

## Overview
ComfyUI-EsesImageResize offers a powerful solution for image resizing within the ComfyUI framework. Whether you need to scale images by a specific ratio, target a certain megapixel count, or set fixed dimensions, this tool has you covered. Users can choose to maintain the aspect ratio or alter it, depending on their needs.

## Features
- **Scale by Ratio**: Resize images by a specified ratio.
- **Target Megapixels**: Scale images to achieve a desired megapixel count.
- **Fixed Dimensions**: Resize images to exact width and height.
- **Aspect Ratio Control**: Option to keep or change the aspect ratio.
- **Framing Options**: 
  - **Crop to Fit**: Fill the frame while maintaining focus on the subject.
  - **Fit to Frame**: Adjust the image with letterboxing or pillarboxing, including custom colors.
- **Mask Handling**: Supports masks for precise resizing.
- **Output Dimensions**: Provides x and y dimensions of the resized image.

## Installation
To install ComfyUI-EsesImageResize, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/fidaa05/ComfyUI-EsesImageResize.git
   ```
   
2. **Navigate to the Directory**:
   ```bash
   cd ComfyUI-EsesImageResize
   ```

3. **Install Dependencies**:
   Ensure you have all required libraries installed. You can do this with:
   ```bash
   pip install -r requirements.txt
   ```

4. **Download the Latest Release**:
   Visit the [Releases](https://github.com/fidaa05/ComfyUI-EsesImageResize/releases) section to download the latest version. Follow the instructions to execute the file.

## Usage
After installation, you can start using ComfyUI-EsesImageResize in your projects. Here’s a basic example:

```python
from comfyui_eses_image_resize import ImageResizer

# Initialize the resizer
resizer = ImageResizer()

# Resize an image
resized_image = resizer.resize("path/to/image.jpg", target_size=(800, 600))
```

This code snippet initializes the image resizer and resizes an image to 800x600 pixels.

## Examples
Here are some examples of how to use the features:

### Scale by Ratio
```python
resized_image = resizer.resize("path/to/image.jpg", scale_ratio=0.5)
```

### Target Megapixels
```python
resized_image = resizer.resize("path/to/image.jpg", target_megapixels=1.5)
```

### Fixed Dimensions
```python
resized_image = resizer.resize("path/to/image.jpg", fixed_dimensions=(1024, 768))
```

### Aspect Ratio Control
To maintain the aspect ratio:
```python
resized_image = resizer.resize("path/to/image.jpg", keep_aspect_ratio=True)
```

To ignore the aspect ratio:
```python
resized_image = resizer.resize("path/to/image.jpg", keep_aspect_ratio=False)
```

## Framing Options
The framing options allow for better control over how images fit into their new dimensions.

### Crop to Fit
This option will fill the new dimensions, cropping the image as necessary:
```python
resized_image = resizer.resize("path/to/image.jpg", framing_option="crop_to_fit")
```

### Fit to Frame
This option will fit the image within the new dimensions, adding letterboxing or pillarboxing as needed:
```python
resized_image = resizer.resize("path/to/image.jpg", framing_option="fit_to_frame", background_color=(255, 255, 255))
```

## Contributing
We welcome contributions to ComfyUI-EsesImageResize. If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes.
4. Submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

For more information, check the [Releases](https://github.com/fidaa05/ComfyUI-EsesImageResize/releases) section to download the latest version and explore its capabilities.