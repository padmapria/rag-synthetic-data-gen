# Synthetic Test Data Generation for RAG Pipelines

## Overview

This repository provides a Python implementation for generating synthetic test data for Retrieval-Augmented Generation (RAG) pipelines using LangChain, OpenAI, and Ragas.  
The goal is to accelerate RAG pipeline evaluation by reducing data aggregation time and enhancing evaluation depth.

## Features

- Generates synthetic question/ground truth pairs for RAG pipelines  
- Utilizes LangChain, OpenAI, and Ragas for efficient data generation  
- Supports customizable distribution configurations  
- Reduces data aggregation time by up to 90%

## Requirements

- Python 3.8+  
- LangChain  
- OpenAI API key  
- Ragas  
- dotenv

## OpenAI LLM via OpenAI API

- OpenAI provides the API for accessing powerful language models like GPT-3.5 Turbo.  
- In this application, the OpenAI API is used to generate data.  
**Note:** OpenAI immediately revokes the API key if it's exposed publicly. Therefore, ensure you do not expose your API key.

Generate your OpenAI API key here: [Click Here](https://platform.openai.com/account/api-keys)

## How to run this application

1. Clone this git repository from the command prompt:
   ```bash
   git clone https://github.com/padmapria/rag-synthetic-data-gen.git    
   cd rag-synthetic-data-gen
   
2. Create a .env file inside the project folder and store the key as follows. The key is loaded in the Python code:
   ```bash
   OPENAI_API_KEY=YOUR_API_KEY_HERE

3. Refer to the code:
   ```bash
   #### Load API key
   from dotenv import load_dotenv   
   load_dotenv()   
   api_key = os.getenv("OPENAI_API_KEY")
   
4. Provide the sample data that you want to generate synthetic data for. This data can be in any file format, such as .txt, .csv, or .json (e.g., .txt). Note:: use the appropriate loader.
5. The synthetic data generated is stored in a CSV file for future testing purposes.
