# GenAI201
A Streamlit application that helps store owners answer questions about their inventory easily using natural language. This application leverages LangChain to combine the power of Large Language Models (LLMs) with a MySQL database.

Key Features

Natural Language Queries: Ask questions about your inventory in plain English (e.g., "How many t-shirts do we have left for Nike in XS size and white color?").

SQL Generation: The app translates your questions into SQL queries to retrieve accurate data.

Informative Answers: Provides clear and concise answers derived from the database results.

Setup

Clone the repository:

Bash

git clone https://github.com/your-username/store-helper
Install dependencies:

Bash

pip install -r requirements.txt
Set up environment variables:

Create a .env file in the project's root directory.

Add the following variables, replacing the placeholders with your actual credentials:

GOOGLE_API_KEY= db_user= db_password= db_host= db_name=

Run the application:

Bash

streamlit run main.py
Usage

Open the Streamlit app in your web browser (typically at http://localhost:8501).

Type your inventory-related question in the "Question" field.

Click the "Submit" button to get the answer.

Code Structure

main.py: Contains the core Streamlit application logic.

langchain_helper.py: Houses functions for setting up the LangChain pipeline, including:

Few-Shot Prompting: Provides examples (few_shots.py) to guide the LLM on how to interact with the database.

SQL Database Integration: Connects to your MySQL database.

LLM (Google PaLM): Used to understand questions and generate SQL queries.

Vector Store (Chroma): Efficiently finds the most relevant examples for the question.

