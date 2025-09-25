```python
from PIL import Image
import os

# List of image file paths
image_files = ['image1.jpg', 'image2.png', 'image3.bmp']

# Convert images to RGB and open them
images = [Image.open(img).convert('RGB') for img in image_files]

# Save as a single PDF
if images:
  images[0].save('merged.pdf', save_all=True, append_images=images[1:])
