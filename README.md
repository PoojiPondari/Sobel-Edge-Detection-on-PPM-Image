# Sobel-Edge-Detection-on-PPM-Image
Sobel Edge Detection on PPM Image
Overview
This program performs edge detection on a PPM image using the Sobel operator, a well-known technique for identifying edges within an image. The Sobel filter computes gradients in both the x (Gx) and y (Gy) directions to highlight the boundaries and changes in intensity. The resulting image highlights edges with black pixels on a white background.

Features
Edge Detection: Implements the Sobel operator to detect edges in an image.
Thresholding: Allows the user to set a threshold to determine which edges are significant enough to be retained.
PPM Image Processing: Handles images in the PPM format for both reading and writing.
Getting Started
Requirements
A C compiler (Tiny C or any other C compiler).
A PPM image file (.ppm) to test the edge detection.
The program reads and writes PPM files using basic image manipulation.
Installation
Clone the repository or download the source code.
Compile the program using a C compiler (e.g., Tiny C, GCC).
bash
Copy code
gcc -o sobel_edge_detection sobel_edge_detection.c
Run the program:
bash
Copy code
./sobel_edge_detection
Usage
Enter the input image file name: The program will prompt you to enter the name of the PPM image file on which you want to apply edge detection.
Enter the threshold value: The threshold value determines the sensitivity of edge detection. Higher values make the program detect only stronger edges, while lower values will detect more subtle edges.
Output: The program will process the image and save the output as edge.ppm, where edges will appear as black pixels on a white background.
Example
bash
Copy code
Enter image file name (with .ppm extension): input_image.ppm
Enter threshold value for edge detection: 50
Edge detection complete. Output saved as 'edge.ppm'.
File Format
Input: PPM image file (P6 format).
Output: Processed PPM image file with edge detection applied (edge.ppm).
How It Works
Sobel Filter: The program applies two Sobel filters (Gx and Gy) to compute the gradients of each pixel in both horizontal and vertical directions.
Gradient Magnitude: The program calculates the edge magnitude at each pixel by combining the horizontal and vertical gradients using the Euclidean distance formula.
Thresholding: After computing the gradient magnitudes, the program compares them to the user-defined threshold. If the magnitude is above the threshold, the pixel is marked as an edge (black); otherwise, it remains white.
Example Output
The result is an image where edges are represented by black pixels, and all other regions are white, making the edges stand out clearly.

License
This project is open-source. You can use, modify, and distribute it as you see fit.
