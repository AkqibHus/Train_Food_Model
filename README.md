# Train_Food_Model
This code sets up a food classification model using the FastAI library, with the primary goal of identifying various food items from the "Food-101" dataset. Here’s a breakdown of the process:

Data Preparation: The dataset is downloaded, containing 101,000 food images across 101 categories. The code parses and filters the JSON file with image labels to select 10 specific categories (e.g., cheesecake, ice cream, nachos).

Image Labeling: The code renames image files to include the food item label in the filename. Unwanted images are removed, reducing the dataset to only the selected food classes.

Data Loading and Transformation: An ImageDataLoaders object is created with an 80-20 split for training and validation. Images are resized to 200x200 for uniform input.

Model Training: A resnet34 CNN model is initialized with transfer learning and fine-tuned for 10 epochs on this specific dataset, aiming to minimize error rates during training and validation.

Model Testing and Prediction: The model can predict labels for uploaded images or random dataset samples, displaying results with probabilities for each class. The predicted label is shown along with a probability distribution for all classes.

This streamlined approach allows the model to classify images into one of the selected food categories, outputting accurate predictions for user-uploaded or test images.
