# Simplilearn-Capstone-Project-Autonomous-Driving

Project Implementation Summary
This project focuses on two major components. The first part involves building a computer vision model to detect objects in images and predict bounding boxes. The second part is a detailed exploratory data analysis of Tesla accident data to identify patterns, trends, and insights related to fatal events.
________________________________________
Part 1: Object Detection Model
1. Dataset Preparation
The process begins by loading a CSV file that contains image IDs, class labels, and bounding box coordinates. Each image is read from the dataset folder, resized to 224x224 pixels, and normalized for model training. Bounding box coordinates are also scaled so that the model can learn in a consistent format.
To support classification, class labels are encoded into numerical values. For better data organization and visualization, the images are then sorted into folders based on their class labels.
2. Data Generation for Training
To improve performance and reduce overfitting, an ImageDataGenerator is used. This automatically handles image preprocessing and splits the dataset into training and validation groups. It allows the model to see more variation in the images.
3. Model Architecture
A custom Convolutional Neural Network is created using TensorFlow and Keras. The model takes an image as input and processes it through several convolutional layers. From these features, the model generates two outputs:
1.	A bounding box with four predicted values (x_min, y_min, x_max, y_max)
2.	A predicted class label for the object in the image
The model is trained using two loss functions. Mean squared error is used for bounding box regression and categorical cross-entropy is used for classification. The Adam optimizer helps the model learn efficiently.
4. Model Training and Evaluation
The model is trained for several epochs, using both the image array and the encoded labels. After training, the loss and accuracy graphs are plotted to understand how the model learned.
A sample test image is then fed into the model. The predicted class and bounding box are printed. The bounding box is drawn on the image to visually verify the result.
________________________________________
Part 2: Exploratory Data Analysis of Tesla Fatal Accidents
1. Data Cleaning and Preparation
The Tesla accident dataset is loaded and inspected for missing values, incorrect formats, duplicates, and unnecessary columns. Several irrelevant or mostly empty columns are removed.
Data types are cleaned and converted wherever needed. Dates are standardized and broken down into year, month, and day. Duplicate and incomplete rows are removed so that the analysis is accurate and reliable.
2. Event Distribution Analysis
A thorough breakdown of accident frequency is performed. The dataset is explored through multiple angles, such as:
•	Number of events each year
•	Number of events by date
•	Number of accidents on each day of the week
•	State-wise and country-wise accident distribution
These insights are visualized through line plots and bar charts to highlight trends and high-risk areas.
3. Analysis of Death-Related Factors
The next part of the analysis focuses on understanding patterns related to fatalities. Several questions are explored, including:
•	How many people died in each accident
•	How many events involved a Tesla driver fatality
•	How many events involved occupant deaths
•	How often cyclists or pedestrians were involved
•	How many cases involved both Tesla occupants and pedestrians or cyclists
•	How often Teslas collided with other vehicles
Clear visualizations are used to show distributions and frequency counts for better interpretation.
4. Model-Based Accident Insights
The accidents are grouped by Tesla model to understand which models are most frequently involved in fatal incidents. Bar plots help highlight this distribution.
Finally, the dataset is explored to identify how many verified autopilot-related deaths occurred. Accidents are also grouped based on whether autopilot was claimed to be involved.
________________________________________
Conclusion
This project combines deep learning and data analysis to provide a complete end-to-end understanding of autonomous vehicle performance and real-world accident outcomes.
Part 1 showcases the implementation of an image-based object detection model that predicts both classes and bounding boxes.
Part 2 provides detailed insights into Tesla accident data, highlighting patterns related to fatalities, vehicle models, locations, and autopilot involvement.
Together, both parts offer meaningful insights into computer vision and real-world autonomous driving data, making this project a strong example of practical machine learning and analytical skills.

