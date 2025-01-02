
# Implementation of PCA with ANN Algorithm for Face Recognition




## Overview
This project implements a face recognition system using Principal Component Analysis (PCA) for dimensionality reduction and feature extraction, coupled with an Artificial Neural Network (ANN) for classification. The system processes facial images and evaluates its performance through various experiments, including the effect of dimensionality reduction and recognition of impostors.
## Libraries Used
- **Numpy:** For numerical computations, including matrix operations and eigenvalue decomposition

- **Scipy:** For advanced scientific computing, such as Singular Value Decomposition (SVD).

- **OpenCV:** For image processing, including reading and preprocessing facial images.
## Project Structure
- **Face Database Generation:** Conversion of face images into a matrix form suitable for PCA.

- **Dimensionality Reduction Using PCA:** Extraction of key features from facial images.

- **Signature Generation:** Representing each face with reduced features.

- **Classification Using ANN:** Training an ANN to classify faces based on their signatures.

- **Testing and Evaluation:** Testing the system with new data and analyzing its performance.
## Steps Involved in Training
1. Generate the Face Database
2. Mean Calculation



3. Subtract the mean face from each face image to obtain mean-zero data.

4. Calculate Covariance of Mean-Aligned Faces

5. Eigenvalue and Eigenvector Decomposition



6. Generate Feature Vectors.
 - Sort the eigenvalues in descending order and select the top  eigenvectors to form the feature vector matrix .

7. Generate Eigenfaces


8. Generate Face Signatures

9. Train ANN
- Use the face signatures  as input features to train an ANN with backpropagation.




## Steps Involved in Testing
1. Prepare Test Image

- Convert the test image into a column vector .

2. Mean Zero Test Data

- Subtract the mean face from the test image to obtain:

3. Project Test Face onto Eigenfaces

- Compute the projected test face :

4. Classification

- Use the trained ANN to classify the test face based on its signature .
## Evaluation Metrics
1. **Effect of  on Accuracy**

- Vary the number of eigenvectors  and evaluate classification accuracy.

- Plot accuracy against  to analyze the trade-off between dimensionality and performance.

2. **Impostor Detection**

- Test the system with images not present in the training set (impostors).

- Evaluate the system’s ability to reject these as not enrolled.




## Results and Insights
- The relationship between  and classification accuracy is visualized and analyzed.

- The system’s robustness against impostors is tested.
## Conclusion
This project demonstrates the effectiveness of PCA for dimensionality reduction and ANN for classification in face recognition tasks. By analyzing the impact of eigenvector selection () and evaluating against impostors, the system’s performance is comprehensively assessed.