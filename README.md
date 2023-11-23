# Image-Compression
This is my first AI/ML Project using unsupervised algorithm
In this project we are using K-Means Algorithm for image compression by reducing the number of colours that occur in the image to only those that are most common in the image.
K-Means algorithm is the method to automatically cluster similar data points togeather. It is a type of unsupervised learning algorithm where we dont have to train the model beforehand. It is an iterative procedure that guesses the intial centroids and refines the position of the centroids based on the mean value of the data points.

Though we can directly using the scikit library, I have tried to do without using those libraries, so that we can get a better peek into the working of algorithm
# How It Works
In a straightforward 24-bit color representation of an image, each pixel is represented as three 8-bit unsigned integers (ranging from 0 to 255) that specify the red, green and blue intensity values. This encoding is often refered to as the RGB encoding. 
Our image contains thousands of colors, and in this part of the exercise, you will reduce the number of colors to 4 colors.
By making this reduction, it is possible to represent (compress) the photo in an efficient way. 
Specifically, you only need to store the RGB values of the 4 selected colors, and for each pixel in the image you now need to only store the index of the color at that location (where only 4 bits are necessary to represent 4 possibilities).

In this part, we will use the K-means algorithm to select the 4 colors that will be used to represent the compressed image.
Concretely, we will treat every pixel in the original image as a data example and use the K-means algorithm to find the 4 colors that best group (cluster) the pixels in the 3- dimensional RGB space. Once you have computed the cluster centroids on the image, you will then use the 4 colors to replace the pixels in the original image.
