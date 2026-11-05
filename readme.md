Network Protocol Classification Using Machine Learning

📌 Project Overview

This project focuses on classifying network protocols using Machine Learning techniques based on network packet information.

The objective is to explore network traffic data, perform data preprocessing and feature engineering, visualize protocol distributions, and train multiple machine learning classification models to identify network protocols.

The project uses packet-level information such as packet length and time-related features to predict the corresponding network protocol.

🎯 Objectives

- Understand and analyze network traffic data.
- Perform data cleaning and preprocessing.
- Explore network protocol distributions through Exploratory Data Analysis (EDA).
- Extract meaningful features from packet timestamps.
- Apply machine learning classification algorithms.
- Evaluate and compare different classification models.
- Identify important features influencing model predictions.

📂 Dataset

Dataset: KT_GameBox Dataset (Merged)

The dataset contains network packet information, including:

- Time
- Source
- Destination
- Protocol
- Length
- Info

Note: The original dataset is not included in this repository due to project and dataset-sharing restrictions. The dataset must be obtained separately and uploaded to Google Colab before executing the notebook.

⚙️ Project Workflow

1. Dataset Loading: Load the merged network traffic dataset using Pandas.

2. Data Understanding: Examine dataset dimensions, columns, data types, statistical summaries, and missing values.

3. Data Cleaning: Handle missing values and remove records with missing protocol labels.

4. Exploratory Data Analysis (EDA):
   
   - Analyze network protocol distribution.
   - Examine packet length distribution.
   - Visualize packet length using histograms and boxplots.

5. Feature Engineering: Extract Hour, Minute, and Second from packet timestamps.

6. Feature Selection: Select the following four features:
   
   - Length
   - Hour
   - Minute
   - Second

7. Encoding: Convert categorical protocol labels into numerical representations using LabelEncoder.

8. Train-Test Splitting: Divide the dataset into training and testing sets using an 80:20 stratified split. Protocol classes with fewer than two records are excluded to enable stratification.

9. Feature Scaling: Apply StandardScaler for the scaled model inputs.

10. Model Training and Evaluation: Train and evaluate multiple machine learning classification algorithms.

🤖 Machine Learning Algorithms

The following algorithms are implemented:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest

📊 Model Evaluation

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

A comparison of model accuracy is also performed to examine their classification performance.

Additional Analysis:

- Random Forest feature importance.
- Decision Tree visualization.
- Prediction of network protocols for a new packet.

🛠️ Technologies Used

Category| Tools / Libraries
Programming Language| Python
Data Manipulation| Pandas, NumPy
Data Visualization| Matplotlib, Seaborn
Machine Learning| Scikit-learn
Development Environment| Google Colab
Version Control| Git, GitHub

🚀 How to Run the Project

1. Clone this repository:
   
   git clone <your-repository-url>

2. Open the ".ipynb" notebook in Google Colab.

3. Upload the separately obtained dataset:
   
   "KT_GameBox_All_Merged.csv"

4. Ensure the dataset is available at:
   
   "/content/KT_GameBox_All_Merged.csv"

5. Execute the notebook cells sequentially.

6. Observe the visualizations, model evaluation reports, confusion matrices, and prediction results.

📁 Repository Structure

Network-Protocol-Classification/
│
├── Network_Protocol_Classification.ipynb
├── README.md
└── requirements.txt

⚠️ Limitations

- The dataset contains an imbalanced distribution of network protocol classes.
- Protocol classes with fewer than two records are excluded during stratified splitting.
- KNN evaluation is performed on a representative subset of 10,000 test samples due to computational requirements.
- Classification performance depends on the selected features and dataset distribution.
- The current implementation uses only four numerical features and does not incorporate all available packet information.

🔮 Future Improvements

- Explore additional network traffic features.
- Apply techniques to handle class imbalance.
- Improve classification performance for minority protocol classes.
- Experiment with additional machine learning algorithms.
- Optimize model performance for large-scale network traffic datasets.