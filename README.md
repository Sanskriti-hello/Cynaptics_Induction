# Cynaptics_Induction
Develop and algorithm to distinguish between Real world and AI generated images utilizing various ML techniques such as image classification. The second sub task of the problem demands training a GAN and using it to classify images. 
## SubTask1: AIvsReal
The purpose of this task was to make us learn CNNs and Model Evaluation.
1. Dataset Preparations: Organize the raw image data into a structured format suitable for training. In the code, I used a loop which will iterate through the directories and assign the label specified. I also converted the text labels of AI and Real as 0 and 1 repectively(Label Encoding).
2. Custom Dataset: Handle image loading and preprocessing for both training and testing datasets. Basically (not required here though) every image even if it's grey scale for such kind of tasks should be first converted to RGB and then transforming it(basically resizing it and normalising the pixels which I have specified later in the code too).
3. Model Definition: Design a convolutional neural network (CNN) for feature extraction and classification. Here, it is a CNN designed for binary classifcation we first work on feature extraction, by Conv2d,ReLu,MaxPool which are repeated 4 times for more complex feature to be transmitted tot he next layer. The classification head takes the extracted features and predicts the probability of each class.
4. Training Model: Gradually improves model performance over multiple epochs.
5. Test Dataset: (Removed image_62 due to error)
(Extra info: Now to improve the accuracy, I tried doing image augmentation too like image jitter, roation and flip but it didn't go as expected)

## SubTask2: GAN
The purpose of this task was to make us learn GANs.
1. Generator Model: The generator's job is to create fake images from random noise. It takes a small vector of random values and transforms it into a full-sized image through a series of layers. Each layer of the generator works to gradually upsample or enlarge the noise, turning it into a more complex and detailed image.
2. Discriminator Model: Binary classifier that distinguishes between real and fake images.
3. Training: The function uses Binary Cross-Entropy Loss to train both networks.
4. The Generator's output is visualized after every 10 epochs, showing how the generated images improve over time. This helps monitor the progress and stability of the GAN.
