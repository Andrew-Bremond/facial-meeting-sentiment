Read the Room: Facial Expression Recognition
CS205: Artificial Intelligence (Fall 2025) | Andrew Bremond

Overview
In interviews and online meetings, it can often be difficult to tell if your answers are landing well or making things awkward. "Read the Room" is a Computer Vision project designed to provide "live feedback" to a speaker by classifying the facial expressions of the person they are talking to.

By estimating what the other person is sensing and feeling, this tool categorizes emotions and aggregates them into a Sentiment Score (Positive, Negative, or Neutral) to help visualize how a conversation is trending over time.

Dataset
This project uses the FER2013 (Facial Expression Recognition 2013) dataset.

Format: Grayscale images of faces, originally 48x48 pixels.

Categories: 7 distinct emotion classes:

0 = Angry

1 = Disgust

2 = Fear

3 = Happy

4 = Sad

5 = Surprise

6 = Neutral

Methodology
1. Preprocessing
Resizing: Images are resized to 224×224 to accommodate standard pre-trained architectures.

Normalization: Pixel values are normalized for stable training.

Splitting: Data is divided into standard train, validation, and test sets.

2. Models Evaluated
Dense Baseline: A simple, fully connected network used to establish a baseline performance metric.

Custom CNN: A lighter Convolutional Neural Network built from scratch, aiming for decent accuracy with limited compute.

ResNet50: A transfer-learning setup utilizing a deep, pre-trained architecture to extract more complex features.

3. Training Techniques
To optimize training on a small dataset, the following techniques were applied:

Data Augmentation

Class Weights (to handle imbalanced emotion classes)

Early Stopping

Results & Conclusion
Performance: Convolutional models (Custom CNN and ResNet50) clearly beat the simple dense baseline and match expectations for a dataset of this size.

Future Scope: Modern state-of-the-art Facial Expression Recognition (FER) utilizes very deep CNNs (like DenseNet), Vision Transformers (ViTs), and facial-landmark mapping. Reaching true SOTA performance for this tool would require larger datasets, those stronger architectures, and higher-quality image labeling.
