# Auto-Insurance-Fraud-Detection 🚗
Data Science project focused on detecting fraudulent auto insurance claims.

This project employs a machine learning classification algorithm to identify fraudulent auto insurance claims. By analyzing data such as insurance policies and accident reports, the algorithm classifies claims as either fraudulent or legitimate with high accuracy. This approach enhances fraud detection and streamlines the claim processing workflow.

![traffic-signs-464641_1920-1](https://github.com/user-attachments/assets/2fcf7e1c-91a7-4661-97bf-344796aad03b)


### Technologies 💻
- Programming Language: Python
- Main Libraries: NumPy, Pandas, Scikit-Learn
- AutoML Frameworks: PyCaret, AutoGluon 
- Data Visualization: Matplotlib, Seaborn, PowerBI
- Machine Learning: Classification Models
- Version Control: Git, GitHub
- Organization: Trello (Kanban Methodology), Miro

### Objectives 🎯
Vehicle insurers handle a large number of accident and damage claims each year. However, a significant portion of these claims may be fraudulent. Detecting fraudulent claims is crucial to reduce financial losses for insurance companies and keep insurance premiums fair for all customers.

For these reasons, the use of advanced prediction techniques to detect fraudulent claims is becoming increasingly crucial.

Therefore, we have decided to implement a fraud detection model for auto insurance that could significantly enhance the company's ability to identify fraud, support fraud prevention analysts, and direct the company’s financial resources towards claims with a higher likelihood of being fraudulent.

### Dataset 🗂️
- The dataset, sourced from Kaggle, contains 15,420 rows and 33 columns, including information such as vehicle details, accident data, and other relevant attributes.
- The target variable is to determine whether a claim application is fraudulent or not, represented by FraudFound_P.
  
![2024-08-26 12_48_29-● 1 IF Exploración datos ipynb - Caso Insurance - Visual Studio Code](https://github.com/user-attachments/assets/22b6ff3e-3f5f-4dd7-83f5-8fdf4890f96c)

### EDA 📈
We can see a preview of some elements of the exploratory analysis


![image](https://github.com/user-attachments/assets/f5423ef5-77ff-43a5-9375-789b13eec6cf)

![image](https://github.com/user-attachments/assets/bef58645-fa71-42f7-8d71-c2368c96cb37)

![2024-08-26 15_33_53-Presentación Detección de Fraude pptx - Microsoft PowerPoint Online - Brave](https://github.com/user-attachments/assets/30905f66-683b-4c62-9500-d35e95dbe36a)



### Models ⚙️
- We evaluated several models using PyCaret, including: Gradient Boosting Classifier (GBC), Logistic Regression, LightGBM, XGBoost. Each model was assessed based on various performance metrics to determine its effectiveness in detecting fraud.
- Selected Model: We have chosen the Gradient Boosting Classifier as our final model. 
- GridSearch was applied to the Gradient Boosting Classifier to optimize hyperparameters and improve model performance.
- Train and test metrics were compared to assess possible overfitting.

### Metrics
The performance of the Gradient Boosting Classifier (GBC), the selected model, was evaluated using key metrics on both the training and test sets. Below are the results:
![image](https://github.com/user-attachments/assets/58bc5290-24dd-4ba1-a6e3-b001a844fba1)

### Key Results
- Accuracy: The model achieved high accuracy on both the training set (0.98) and the test set (0.96). This indicates that the model generalizes well with minimal overfitting.
- AUC-ROC: The AUC-ROC score is close to 1, with a value of 0.99 for both datasets, demonstrating the model's strong ability to distinguish between fraudulent and non-fraudulent claims.
- Precision: The precision of 66.8% on the test set indicates that when the model predicts fraud, it is correct approximately 66.8% of the cases. This suggests a significant number of false positives.
- Recall: The recall of 98.2% on the test set shows that the model successfully detects 98.2% of fraud cases. This is a strong performance, as the primary goal is to identify as many fraud cases as possible.
- F1 Score: The F1 score of 79.5% on the test set reflects a good balance between precision and recall. While the F1 score indicates that the model effectively balances both aspects, the relatively low precision (66.8%) suggests there is room for improvement in the model’s performance.

### Challenges and Limitations
In this project, we faced several challenges and limitations that were addressed through targeted strategies:

- Severe Class Imbalance in the Dataset - Solution: Applied SMOTE technique to balance the dataset.
- High Proportion of Categorical Variables - Solution: Used OneHotEncoder for encoding and created additional features.
- Default decision threshold (0.5) was not optimal for maximizing the model's sensitivity - Solution: Adjusted the threshold to 0.2 to improve sensitivity.
- Risk of Overfitting - Solution: Performed additional techniques, such as cross-validation, increased training data, and hyperparameter tuning, to mitigate it.

### Conclusions 📝
- Despite these challenges, the model performs well with good detection rates. While there is still room for improvement, it meets the requirements and generally gives reliable results.
- 
### Future Improvements 🔧
- Implementation of a scoring system that classifies clients based on their risk level.
- Development of a regression model to predict the amount of fraud by requesting additional data (e.g., fraud amount) from the client.
- Ongoing evaluation of the model
- Incorporate external data (known fraud databases and socioeconomic data)
- Implement a continuous feedback system
  
### Team 👥
This project has been created by: Flora Comesaña & Noelia Beltrán
