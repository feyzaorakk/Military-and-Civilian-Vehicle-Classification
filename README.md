# Military and Civilian Vehicles Classification

## Team Members
- Bican Çağrı GÖKSEL, goksel20@itu.edu.tr, https://github.com/cagrigoksel
- Feyza ORAK, orakf20@itu.edu.tr

## Overall Process
- Data Preprocessing
- Pretrained Model Selection & Hyperparameter Tuning
- Ensemble Modelling

## Data Set Introduction
- The dataset consists of images of various vehicles of two types, military and civilian. There 6772 images in total. 717 of them belongs to test set and the rest belongs to train set. Each image is labeled according to the vehicle type, which is very important for training the classification model. The classes are as follows:

    - Civilian aircraft
    - Civilian car
    - Military aircraft
    - Military helicopter
    - Military tank
    - Military truck

## Description of the Problem
- The project aims to build a classifier to predict vehicle types based on visual data. The approach involves exploring various models such as EfficientNet, DenseNet and ResNet to determine the best-performing model.
- Key questions addressed include:
  - How can we accurately classify images of vehicles into their respective categories?
  - What preprocessing techniques enhance model performance?
  - What types of models can be used in image classification?
  - How do different models compare in terms of accuracy and efficiency?

## Data Exploration
- Visualizations were created to provide insights into the data, such as the number of images per class. This helped in identifying any class imbalances and understanding the data better.
- Duplicated datas were checked and removed due to prevent any repetitive information during the training process.
- Null values are controlled to see if we have any missing information. Despite of the checking, there was not a null value in our dataset so we did not have to drop any of the rows.

## Methodologies
- Data preprocessing techniques included resizing images to a uniform size (400x250 pixels), normalizing pixel values, and augmenting the dataset to improve model robustness.
- The project utilized PyTorch for model training, employing transfer learning with pre-trained models. Hyperparameter tuning was performed using Optuna to optimize model performance.
- Deep neural networks (DNNs) are ideal for image classification because they can automatically learn hierarchical feature representations from raw pixel data, enabling them to recognize complex patterns and objects in images. DenseNet, EfficientNet, and ResNet are particularly effective choices because DenseNet supports efficient feature reuse with its dense connections, improving performance and reducing parameters; EfficientNet balances network depth, width, and resolution to maximize accuracy while minimizing computational cost; and ResNet uses residual connections to allow much deeper networks to be trained without suffering from vanishing gradients, increasing the model’s ability to learn complex features from large datasets. Therefore, these three models were used for model selection.
- An ensemble model was developed by combining predictions from multiple models to improve accuracy. The ensemble approach averaged the outputs of the individual models, leading to better performance on the test set.

## Results
- The best model was selected based on validation accuracy, achieving an overall accuracy of 90% on the test set. The classification report indicated strong performance across all vehicle categories, with precision, recall, and F1-scores above 0.87 for most classes.
- The ensemble model, which combined DenseNet121, ResNet50, and EfficientNetB0, further improved performance, achieving an accuracy of 93% on the test set. This demonstrates the effectiveness of combining multiple models to enhance prediction reliability.

## Conclusion
- The project was carried out with training using deep learning models for the classification of military and civilian vehicles.
- The project successfully demonstrated the application of deep learning techniques for image classification tasks, achieving satisfactory results with the selected models. The ensemble model, in particular, showcased the potential for improved accuracy through model combination.
- Future work could explore additional data augmentation techniques, experiment with more complex models, or apply the methodology to other image classification tasks.

## References
- [Mendeley Dataset](https://data.mendeley.com/datasets/njdjkbxdpn/1)

## Additional Folders
- [Image and Label Folder](https://drive.google.com/drive/folders/19zN-tfE5l95oTFO84kqXiaULpq3qTusb)
