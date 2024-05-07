Color Palette Extractor
This Python script extracts the dominant color palette from an image using k-means clustering.
Dependencies
matplotlib
pandas
scipy
sklearn
seaborn
Usage
Install the required dependencies.
Place your image file (e.g., "my_image.jpg") in the same directory as the script.
Modify the num_dominant_colors variable in the script to specify the number of colors you want to extract.
Run the script: python ColorPalette.py
The script will display the extracted color palette as an image.
How it Works
Read the image: The script uses matplotlib.image to read the image file.
Extract RGB values: It loops through each pixel and extracts the red, green, and blue values.
Create a DataFrame: The RGB values are stored in a pandas DataFrame.
Scale the data: The RGB values are scaled using scipy.cluster.vq.whiten to ensure that each color component has equal importance in the clustering process.
K-means clustering: The script applies k-means clustering with the specified number of clusters (dominant colors) to group similar colors together.
Extract cluster centers: The centers of the clusters represent the dominant colors in the image.
Unscale the data: The cluster centers are unscaled to obtain the actual RGB values of the dominant colors.
Display the palette: The extracted color palette is displayed as an image using matplotlib.pyplot.
Example
The provided ColorPalette.py script uses an image named "spongebob.jpg" and extracts the 10 most dominant colors. You can replace this with your own image and adjust the number of colors as needed.
