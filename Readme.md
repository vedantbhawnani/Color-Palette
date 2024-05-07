# Color Palette Extractor

This Python script extracts the dominant color palette from an image using k-means clustering.

## Dependencies

* matplotlib
* pandas
* scipy
* sklearn
* seaborn

## Usage

1. **Install the required dependencies.**
2. **Place your image file (e.g., "my_image.jpg") in the same directory as the script.**
3. **Modify the `num_dominant_colors` variable in the script to specify the number of colors you want to extract.**
4. **Run the script:** `python ColorPalette.py`
5. **The script will display the extracted color palette as an image.**

## How it Works

1. **Read the image:** The script uses `matplotlib.image` to read the image file.
2. **Extract RGB values:** It loops through each pixel and extracts the red, green, and blue values.
3. **Create a DataFrame:** The RGB values are stored in a pandas DataFrame.
4. **Scale the data:** The RGB values are scaled using `scipy.cluster.vq.whiten` to ensure that each color component has equal importance in the clustering process. 
5. **K-means clustering:** The script applies k-means clustering with the specified number of clusters (dominant colors) to group similar colors together.
6. **Extract cluster centers:** The centers of the clusters represent the dominant colors in the image.
7. **Unscale the data:** The cluster centers are unscaled to obtain the actual RGB values of the dominant colors.
8. **Display the palette:** The extracted color palette is displayed as an image using `matplotlib.pyplot`.

## Example 

The provided `ColorPalette.py` script uses an image named "spongebob.jpg" and extracts the 10 most dominant colors. You can replace this with your own ima
