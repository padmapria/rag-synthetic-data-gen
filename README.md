# Synthetic Test Data Generation for RAG Pipelines

<h2> LLM & RAG  </h2>
- Large language models (LLM) can be used in variety of tasks including answering questions, writing essays & etc. But have limitations in tasks requiring external knowledge (for example, our knowledge base that is our private data) and factual information. For ex, if i ask Language model how much I spent this month, LLM wont be able to tel as its not trained on that data. <br/>
<br/>
- Retrieval-augmented generation (RAG) integrates external information retrieval into the process of generating responses by Large Language Models (LLMs). <br/>
![image](https://github.com/padmapria/LM-RAG-Chatbot-over-custom-data/assets/31624929/9fb2e6bd-6998-47fd-aebd-cdd8663eb673)

<h2> Synthetic data  </h2>
- Synthetic data refers to artificially generated information that mimics the characteristics of real-world data, but is created through computational methods rather than being collected from actual events or sources. <br/>
- This simulated data is valuable for testing, training, and - research purposes, as it overcomes privacy concerns, data scarcity, and logistical constraints associated with using genuine data.<br/>

## Project Overview

This repository provides a Python implementation for generating synthetic test data from a private datasource for Retrieval-Augmented Generation (RAG) pipelines using LangChain, OpenAI, and Ragas.  
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
