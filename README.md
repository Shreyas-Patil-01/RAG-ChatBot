# RAG-ChatBot
This project involves the development of a machine learning chatbot capable of interacting with a large codebase or repository. It leverages advanced technologies like Qdrant for vector storage, Retrieval Augmented Generation (RAG) for intelligent information retrieval and LLMs, specifically the "Llama 8B" model to process codebases .

# Chatbot for personalized large code bases.

## Table of Contents
- [Project Overview](#project-overview)
- [Objectives](#objectives)
- [Dataset](#dataset)
- [Model Fine-Tuning](#model-fine-tuning)
- [Installation](#installation)
- [Features](#features)
- [Workflow](#workflow)
- [Visual Representation](#visual-representation)
- [Usage](#usage)
- [Contributing](#contributing)


## Project Overview

### Description
This project focuses on building a chatbot that leverages Retrieval Augmented Generation (RAG) along with Large Language Models (LLMs) for interacting with large codebases. The system is designed to take input in the form of a ZIP file, PDF, or GitHub repository, and convert it into a vector database using Qdrant. With the help of LLM (Llama 8B), it then provides users with natural language explanations of the codebase.Further with the help of RAG user can chat with their code base queries. The chatbot is hosted and deployed on AWS SageMaker, making it scalable and accessible.

### Objectives
- **Simplify Query Creation**: Enable users to write queries in plain English, eliminating the need to understand large code base.
- **Enhance Accessibility**: Accesibility increased.
- **Increase Productivity**: Speed up the process of understanding and modifying the large code bases which will reduce lots of time.

### Dataset
The dataset for this project is based on various code repositories (ZIP files or GitHub links) provided by the users. The input dataset is processed to generate vector embeddings using Qdrant, which are later queried to retrieve relevant code snippets and their explanations. This Qdrant will help to create the knowledge graphs.

Additional synthetic datasets may be used during the fine-tuning phase to further train the Llama 8B model for understanding and explaining code structure.

### Model Fine-Tuning
The base model used in this project is Llama 8B. To tailor the model to effectively explain codebases in natural language, fine-tuning is performed. This involves:
Feeding the model code snippets and comments to enhance its contextual understanding.
Vector embeddings created from the codebase are used to help the model generate accurate, context-aware answers.
The fine-tuning process uses the Together AI API, which provides computational resources to adjust and optimize the model for handling large codebases efficiently.

### Installation
Clone this repository and install the required dependencies:
```bash
git clone https://github.com/Shreyas-Patil-01/RAG-chatbot
cd chatbot
```

### Features
- **Natural Language Input**: Users can input their queries in natural language.
- **Accurate Generation tree stucture**: The model generates the accurate tree like structure of the code base.
- **Customizable**: Fine-tuned on a custom dataset to handle specific types of queries relevant to your use case.
- **User-Friendly**: Easy-to-use interface that simplifies the process of complex codes.


### Workflow
1. **Input**: Choose the zip file, pdf or github link as the input.
2. **s3 Bucket**: The provided large code base is stored in the AWS s3 bucket.
3. **Odrant Cluster**: In this we will store the vector embeddings.
4. **Creation of Vectore DB**:Knowledge graphs of the data are created which is very much essential in the RAG.
5. **RAG**:Retrieval Augumented Generation is implimented .
6. **LLM (Llama 8B)**:With the RAG the file is send towards the LLM with the help of "together API" to generate simple natural language tree structure.
7. **Chatbot**:Final chatbot created on the top of the knowledge graphs layer.Further deployed on the AWS Sagemaker.

### Visual Representation
![Project Workflow](https://github.com/Shreyas-Patil-01/RAG-ChatBot/blob/main/workflow.jpg)
![Project Workflow](https://github.com/Shreyas-Patil-01/RAG-ChatBot/blob/main/knowledge%20Graph%20generation.png)
![Tree structure of codebase](https://github.com/Shreyas-Patil-01/RAG-ChatBot/blob/main/tree%20structure.png)
![Tree structure of codebase](https://github.com/Shreyas-Patil-01/RAG-ChatBot/blob/main/chatbot%20output.png)

This diagram illustrates the end-to-end process of RAG chatbot.


### Usage
To use this model, follow the steps below:
- 1. Install the necessary dependencies.
- 2. Load the fine-tuned model.
- 3. Input large code base.
- 4. Receive the corresponding PromQL query as output.
- 5. Access through its endpoint by requesting the model.
- 6. **Make sure to connect the AWS account for s3 bucket , Qdrant account and Together AI API**

### Contributing
Further any contribution related queries : shreyaspatil4780@gmail.com
