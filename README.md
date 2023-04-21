This project presents the implementation and evaluation of an image search engine as part of the Dublin City University MSc Computer Science (Artificial Intelligence) program, CA6005 Mechanics of Search Assignment 2. It discusses the implementation and evaluation to find the most similar images to a given query image using deep learning techniques. The InceptionV3 model is used to extract features from the images, and the cosine similarity is computed between the feature vectors to measure the similarity between the images. The code consists of several parts, including importing necessary libraries, downloading images, pre-processing the images, computing feature vectors, and finally displaying the top 5 similar images for each query image.
First, the necessary libraries are imported, such as TensorFlow for deep learning computations, NumPy for numerical operations, and matplotlib for data visualization. Additionally libraries are installed if they are not already present in the system, such as icrawler for downloading images and scikit-learn for computing cosine similarity.
Next, the code downloads images of 2 specific animals – “cats” and “porcupines” using the GoogleImageCrawler class from the icrawler library. The images are saved in a specified directory “query”, and the crawler is set up with the desired number of threads for feeding URLs, parsing HTML pages, and downloading the images.
After downloading the images, the InceptionV3 model is loaded, and a function is defined to preprocess the input images to make them compatible with the InceptionV3 model. Another function is defined to get the predicted labels for the input images, and the image surrogates are written to a CSV file.
The feature vectors for all the images in the "animals" directory are computed using the InceptionV3 model, and a function is defined to compute feature vectors for a list of images. The feature vectors for all the images in the "query" directory are also computed.
Finally, the cosine similarity matrix between the images in the "query" and "animals" directories is computed, and the top 5 similar images to each image in the "query" directory are displayed along with their similarity index.
