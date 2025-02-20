# Image Augmentation Package

## Overview

This package provides a set of functions for image augmentation using various techniques. Users can integrate these functions into their projects to preprocess images for machine learning tasks or other applications.

## Features

- **Image Augmentation Functions**: Includes functions for flipping, rotating, shearing, cropping, blurring, adjusting exposure, adding noise, and more.
- **Flexible Integration**: Functions can be used individually or combined based on user requirements.
- **Output Options**: Generates augmented images in a specified output directory, with options to create ZIP or TAR.GZ archives.

## Installation

To install the package, you can use pip:

```bash
pip install amplifyy==0.1
```

## Usage

### Example Usage

```python
from amplifyy import (
    get_custom_augmented_images,
    get_augmentation_descriptions,
    apply_all_augmentations,
    create_zip,
    create_tar_gz_with_timestamp
)

input_dir = 'path/to/input/directory'
output_dir = 'path/to/output/directory'

# Display available augmentations with their descriptions
augmentation_descriptions = get_augmentation_descriptions()
for method, description in augmentation_descriptions.items():
    print(f'{method}: {description}')

# User selects augmentation methods based on the provided descriptions
user_choices = [1, 2, 3, 4, 5]  # Example choices

# Apply specific augmentations
get_custom_augmented_images(input_dir, output_dir, user_choices)

# Apply all augmentations
apply_all_augmentations(input_dir, output_dir)

# Create a zip file of augmented images
create_zip('augmented_images.zip', output_dir)

# Create a tar.gz file of augmented images with a timestamp
create_tar_gz_with_timestamp(output_dir)
```

### Functions

- **`get_augmentation_descriptions()`**: Returns all augmentation options that can be select by user.

- **`get_custom_augmented_images(input_dir, output_dir, user_choices)`**: Applies selected augmentations to images in `input_dir` and saves augmented images to `output_dir`.
  
- **`apply_all_augmentations(input_dir, output_dir)`**: Applies all available augmentations to images in `input_dir` and saves them to `output_dir`.
  
- **`create_zip(zip_filename, output_dir)`**: Creates a ZIP archive containing augmented images from `output_dir`.
  
- **`create_tar_gz_with_timestamp(output_dir)`**: Creates a TAR.GZ archive with a timestamp containing augmented images from `output_dir`.

Additionally, we have a special command that you can run after installing the package:

```bash
amplifyy
```

What it does is a secret, so try it out and see for yourself!

## License

This project is licensed under the License - see the [LICENSE](https://github.com/Adarshh9/Amplify/blob/main/LICENSE) file for details.

## Acknowledgments

- The script uses the Pillow and OpenCV libraries for image processing.
- Image augmentation functions are adapted from common techniques used in data augmentation for computer vision.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your enhancements.

## Support

For any questions or issues, please [open an issue](https://github.com/Adarshh9/Amplify/issues) on GitHub.
