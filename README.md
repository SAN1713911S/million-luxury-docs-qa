# Million Technical AI Engineer Test

## Overview

This project offers a solution to extract, process, and answer questions based on real estate documents (in PDF format). It leverages the **FLAN-T5** model to provide direct answers to specific questions by quoting relevant content from the document.

## Features

- **Text extraction** from PDF documents using the PyMuPDF library.
- **Text preprocessing** to ensure clean, readable input for the model.
- **Question Answering (QA)** using the FLAN-T5 model, which generates responses based on the document's content.
- **Automatic download** of the pre-trained FLAN-T5 model from Hugging Face.

---

## 📋 Requirements

To run this project, ensure you have the following installed:

- Python 3.x
- PyTorch
- Transformers library from Hugging Face
- Requests library
- PyMuPDF (fitz) for PDF processing

### Installation

To install the required dependencies, run:

pip install torch transformers requests PyMuPDF

### 🚀 Setup Instructions
Download the Project Clone or download the repository to your local machine:

- git clone <repository_url>
- cd <project_directory>
- Download Pre-trained Model The project uses the google/flan-t5-large model. When you run the program for the first time, it will automatically download the model and tokenizer. If you'd like to save the model locally, it will be stored in the ./saved_model directory.

### 🛠 Running the Project
After installing the dependencies and downloading the model, follow these steps to execute the project:

Run the Jupyter Notebook:

- Open the notebook in a Jupyter environment:

- jupyter notebook Million_Technical_AI_Engineer_Test.ipynb

- Extract and Process Text: The script will automatically download the PDF from a provided URL, extract its text, preprocess it, and then generate answers for predefined questions.

- Customize PDF URL and Questions To customize the document or ask different questions, modify the following:

- Change the PDF URL: Update the github_pdf_url variable in the notebook to point to your desired PDF document.

- Edit Questions: Modify the list of questions based on the information you want to extract.

Example of questions in the script:

questions = [
    "What is the delivery date for the South Tower of UNA CLUB?",
    "What is the price range for residences in Brickell Home Luxury?",
    "How many stories does the Bayfront Residences building have?",
    ...
]

### 🧠 How It Works
- Model Loading:
The ModelManager class loads the model and tokenizer, either from Hugging Face or from a local directory if previously saved.

- PDF Text Extraction:
The PDFExtractor class downloads and extracts text from the provided PDF file.

- Text Preprocessing:
The extracted text is normalized by removing extra spaces and cleaning it up for better processing.

- Question Answering:
The QAGenerator class feeds the preprocessed text to the FLAN-T5 model and generates answers to the predefined questions.

- Answer Output:
The answers are printed to the console for each question, providing direct quotes from the document.

### 📊 Example Output
Upon running the script, you can expect output like this:

Q: What is the delivery date for the South Tower of UNA CLUB?
A: "The South Tower is expected to be delivered by December 2025."

Q: What is the price range for residences in Brickell Home Luxury?
A: "Prices range from $750,000 to $1.2 million."

...
### ⚙️ Notes
Model Saving:
- The model and tokenizer will be saved locally after the first download. This prevents re-downloading the model in future runs.

- Text Length Limitation:
The model has a token limit (2048 tokens). For documents longer than this, you may need to truncate or split the text.

- PDF Format:
Ensure the URL you provide points to a raw PDF file (not a webpage or HTML page).

### 📝 License
This project is licensed under the MIT License - see the LICENSE file for details.

###  📚 Contributing
If you would like to contribute to this project, feel free to fork the repository, make your changes, and submit a pull request. Contributions are always welcome!

###  👥 Contact
For further questions or issues, please reach out to:

Email: santiago.nino02.usa@gmail.com

GitHub: https://github.com/SAN1713911S

Thank you for checking out the Million Technical AI Engineer Test project!
