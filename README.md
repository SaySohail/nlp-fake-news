



<h3 align="center">Fake News Detection using Support Vector Machine (SVM) Classifier</h3>

<div align="center">

  [![code coverage](coverage.svg "Code coverage")]()
</div>

---


## 🧐 About <a name = "about"></a>

The pervasive problem of fake news in online platforms necessitates the development of automatic detection methods. In this coursework, I will build and evaluate a text classifier using the Support Vector Machine (SVM) algorithm to detect fake news. The dataset provided contains over 10,000 statements on current affairs, annotated with labels ranging from 'true' to 'pants on fire' to represent different degrees of fakeness. For the purpose of this project, I will simplify the task to a binary classification problem, distinguishing between 'real' and 'fake' news.


### Simple Data Input and Pre-processing:
* Implement the parse_data_line function to extract the label and statement column values from a line of the tab-separated text file.
* Implement the pre_process function to tokenize the text into a list of words.
* Convert the labels to binary values, where 'REAL' is represented as 1 and 'FAKE' as 0.

### Simple Feature Extraction:
* Implement the to_feature_vector function to create a feature vector from a preprocessed text.
* Build a global_feature_dict to keep track of all the tokens/feature names present in the dataset.
* Experiment with different feature weighting schemes such as binary values, term frequency, or term frequency-inverse document frequency (TF-IDF).
### Cross-validation on Training Data:
* Complete the implementation of the cross_validate function to perform a 10-fold cross-validation on the training data.
* Utilize the train_classifier and predict_labels functions to train the SVM classifier and predict labels for validation.
* Calculate evaluation metrics such as precision, recall, F1-score, and accuracy for each fold.
* Compute the average performance metrics and store them in the cv_results variable.

### Error Analysis:
* Examine the performance of the classifier using a confusion matrix to identify false positives and false negatives.
* Conduct an error analysis on a simple train-test split of the training data.
* Print or record the false positives and false negatives for the 'FAKE' label to investigate why the classifier is misclassifying these instances.
* Provide observations and examples in the report to explain the classifier's confusion.
### Optimizing Pre-processing and Feature Extraction:
* Explore various methods to improve the pre-processing stage, considering token filtering, punctuation handling, normalization, lemmatization, and stop-word removal.
* Experiment with different feature types beyond unigram tokens, such as word combinations or character-level features.
* Explore alternative feature weighting schemes and stylistic features like the number of words per sentence.
* Adjust SVM parameters, such as the cost parameter or per-class weighting.
* Perform feature selection techniques to limit the number of features.
* Utilize external resources like publicly available lists to enhance the feature set.
* Document the methods attempted and report their impact on the classifier's performance.
### Using Other Metadata in the File:
* Modify the load_data function to include additional metadata features from the data file.
* Experiment with incorporating these features into the classification model to optimize performance.
* Record the improvements achieved by different features in a results table in the report.
* Clearly document the exploration process and describe the impact of each feature in the notebook.
### Conclusion:
In this project, I have implemented an SVM classifier for fake news detection. By utilizing text classification techniques, I have developed a model capable of distinguishing between real and fake news. I have explored various strategies to optimize the pre-processing stage, feature extraction, and the inclusion of metadata features. The final model's performance was evaluated using cross-validation and error analysis. The findings and improvements made contribute to enhancing the accuracy and effectiveness of fake news detection systems.

## 🔖 Project structure

```
Project_folder/
|- bin/          # contains scripts and main files that should be run
|- config/       # config files
|- notebooks/    # notebooks for EDA, exploration, predictions and results and conclusions
|- src/          # source code - contains functions
|- tests/        # Test files should mirror the src folder
|- Makefile      # automatize taks through make utility
```

## 🏁 Getting Started <a name = "getting_started"></a>
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites
Setup your environement and install project dependencies
```
conda create -n my_project python=3.10
source activate my_project

python -m pip install pip-tools
pip-compile --output-file requirements.txt requirements.in requirements_dev.in
python -m pip install -r requirements.txt
```

### Installing

## 🔧 Running the tests
Tests are implemented in ./tests, you need to run the following command to run them.
```
make tests
```


