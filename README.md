# Image Processing with OpenCV

This Python script uses the OpenCV library to perform various image processing techniques. 
The code includes functionalities for cropping, center circle removal, background removal, transparency, and heatmap generation.

## Requirements

- Python 3.x
- OpenCV
- Matplotlib
- NumPy
- PIL (Python Imaging Library)

## Usage

1. Run the script (`python image_processing.py`).
2. The code reads an input image and performs the following operations:
   - Cropping the image.
   - Removing the center circle.
   - Removing the background.
   - Creating a transparent background.
   - Generating a heatmap.
   - Saving the processed images in the "Output" directory.

## Special Note

This code requires the "Output" directory to be present for writing(saving) images. 
Make sure to create this directory before running the script.


## Functions

1. **Reading the Image:**
   - Reads the input image using OpenCV and displays it.

2. **Cropping the Image:**
   - Converts the image to grayscale.
   - Applies Gaussian blur and detects edges using the Canny edge detector.
   - Dilates the edges and finds the largest contour.
   - Crops the image based on the bounding rectangle of the largest contour.

3. **Center Circle Removal:**
   - Converts the cropped image to grayscale.
   - Blurs the image to find the center circle.
   - Uses HoughCircles to detect circles and fills the largest one in black.

4. **Background Removal:**
   - Converts the cropped and center-removed image to grayscale.
   - Detects edges using Canny and dilates them.
   - Applies a bitwise AND operation to remove irrelevant pixels.

5. **Transparentation:**
   - Converts the image to RGBA mode for transparency.
   - Sets the alpha channel to 0 for pixels with a sum of RGB values less than 30.

6. **HeatMap:**
   - Applies a colormap to the image excluding transparent areas.
   - Combines the colormap image with the transparent image.
   - Generates a heatmap using the Jet colormap.

7. **Heatmapped Image Saving:**
   - Removes blue background from the heatmap using a color threshold.
   - Saves the resulting image in the "Output" directory.
  

## Special Thanks

This code was collaboratively written by the owner of the repository and its collaborators with the assist of ChatGPT. 
Special thanks to my amazing teammates for their contribution and to ChatGPT for assistance in the coding process.


