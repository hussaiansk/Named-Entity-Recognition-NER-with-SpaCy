# Named-Entity-Recognition-NER-with-SpaCy
📄 Automatic Resume Summarization using Named Entity Recognition (NER)

Evaluate resumes at a glance using Named Entity Recognition (NER) to automatically extract key information such as candidate name, education, skills, experience, and organizations.

🚀 Overview

Recruiters often need to evaluate hundreds of resumes in a short period of time. However, resumes frequently contain excessive or irrelevant information, making bulk screening tedious and time-consuming.

This project leverages Named Entity Recognition (NER) — a subfield of Natural Language Processing (NLP) — to automatically extract critical entities from resumes and generate concise summaries for quick evaluation.

The goal is to:

Reduce manual screening effort

Enable faster shortlisting

Improve consistency in resume evaluation

🧠 What is Named Entity Recognition (NER)?

Named Entity Recognition (NER) is a sub-task of information extraction that identifies and classifies entities in text into predefined categories such as:

PERSON (Candidate Name)

ORG (Organizations / Companies)

EDUCATION (Degrees, Institutions)

SKILLS

LOCATIONS

DATES

EXPERIENCE

EMAIL / CONTACT DETAILS

NER systems can be built using:

Rule-based linguistic methods

Statistical machine learning models

Deep learning approaches

Semi-supervised learning methods

In this project, we use a statistical machine learning approach via spaCy.

📊 Dataset
Dataset Creation

To train the model:

220 resumes were collected from an online job platform.

Documents were uploaded to an annotation tool.

Important entities were manually annotated.

The tool generated JSON-formatted training data.

Each JSON entry contains:

Raw resume text

Entity labels with character offsets

Data Split

Training Set: 200 resumes

Test Set: 20 resumes

🏗️ Model Training

We use spaCy’s custom NER pipeline for training.

Training Approach

Statistical prediction-based learning

Minibatch training

Shuffled training data per epoch

Dropout regularization to prevent overfitting

Training Configuration

Epochs: 10

Dropout rate: 0.2

Minibatch optimization used

Dropout helps prevent the model from memorizing the training data by randomly disabling 20% of features during training.

📈 Model Evaluation

The model was tested on 20 unseen resumes.

For each entity, we calculated:

Accuracy

Precision

Recall

F1-Score

The entity-wise scores were averaged to obtain overall model performance.

Results

The model demonstrated:

Strong entity extraction capability

High precision in identifying key resume components

Good generalization on unseen resumes

Predicted summaries were stored as separate .txt files.

📝 Sample Output
Input:

Full-length resume text

Output (Generated Summary):

Name

Education

Skills

Experience

Organizations

Contact Details

This enables recruiters to evaluate candidates within seconds.

🛠️ Tech Stack

Python

spaCy

JSON

Custom annotated dataset

📂 Project Structure (Suggested)
├── data/
│   ├── train_data.json
│   ├── test_data.json
├── models/
│   ├── ner_model/
├── outputs/
│   ├── summarized_resumes/
├── train.py
├── evaluate.py
├── README.md
🔮 Future Improvements

Increase dataset size for better generalization

Use transformer-based models (e.g., BERT, RoBERTa)

Add resume ranking system

Deploy as REST API

Build web interface for recruiters

💡 Why This Matters

Automated resume summarization:

Saves recruiter time

Improves hiring efficiency

Enables scalable candidate screening

Reduces human fatigue in bulk evaluation

🤝 Contributions

Contributions, suggestions, and improvements are welcome!

If you find this useful, consider starring the repository ⭐
DataTurks: Data Annotations Made Super Easy
Data Annotation Platform. Image Bounding, Document Annotation, NLP and Text Annotations. #HumanInTheLoop #AI, #TrainingData for #MachineLearning.
