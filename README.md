# team27_project2_object_recognition
hack-q-thon 2021 project2 submission for team27<br>
Team members: Jun Wei Chow, Hyun Jin Kim, Timsina Ashok, Rifatul Islam Himel<br>

This is a second  project for team 27. This project demonstrates quantum object recognition, classifying automobiles and deer by training and testing with CIFAR-10 database.

## Problem we tried to address: <br>
Deep-learning based image recognition is a key technology for computer vision, artificial intelligence, autonomous vehicles, and urban surveillance. It endows the computer with the ability to “see” and react accordingly. In particular, for autonomous vehicles, or self-driving cars, without the capability to detect other automobiles, passerbys, and possible obstacles, the safety of the passengers would be at jeopardy. The speed of classification is crucial too; since the safety of people is at stake, milliseconds of difference in the processing speed might make a difference. Researchers are therefore striving to discover faster and more accurate neural network models for object classification. From OverFeat, VGG16, Fast R-CNN, to YOLO, various models have been developed, each outperforming their predecessors. Quantum image processing is an emerging field and requires more research. Its potential to speed up certain commonly-used operations such as edge detection is just starting to gain attention. Hence it would be meaningful to explore the power of quantum deep learning and examine its performance in classifying and recognizing images of objects that can be seen on the road. Quantum computing might lead the way to the next breakthrough in enhancing image recognition. <br>

## Solution: <br>
We propose a solution to build a quantum neural network to classify two different types of images: automobiles and deer. We chose to obtain data from the CIFAR-10 database since it contains the most relevant images, such as different types of transportation and animals. From there we additionally filtered images for automobiles and deer to reduce the size of data. We used the tutorial code from tensorflow for MNIST classification as a main reference, and modified the dataset from MNIST to CIFAR-10. Since the shapes of the datasets are very different, with MNIST being 28x28x1 and CIFAR-10 being 32x32x3, we had to edit almost every part of the code. However the process of training and building the quantum model was similar. Firstly, we loaded the data, filtered it into the types of images that we want, and stored each train and test data to different variables. Then we downscaled every image to 4x4 size. Nextly, we converted the data into np.array format and encoded them as quantum circuits. We represented each pixel as a qubit, and then applied an X gate to each qubit that corresponds to the pixel with brightness higher than the threshold value of 0.5. These circuits were then converted to tensors and were used to create a quantum neural network model circuit. We built a two-layered model where each data qubit acts upon a readout qubit. Using this, a Keras model was constructed, which was trained and tested, demonstrating an accuracy of 90%.<br>

## Inspiration and Reference: <br>
Tensorflow tutorial page for MNIST classification: https://www.tensorflow.org/quantum/tutorials/mnist 

## Miscellaneous: <br>

Link to github repo of the first mini project: https://github.com/Wabinab/hackqthon_team27
