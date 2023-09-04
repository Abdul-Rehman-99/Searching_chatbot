# Searching_chatbot
Embeddings based search bot for large datasets

This NLP project has been done using OpenAi Embeddings model "text-embedding-ada-002" and an OpenAI api key. If you use chatgpt you have the key you just need to access or create an OpenAI account to get one. This key is free and you can have access for a limited time. You can search on google how to get your OpenAi key or use this link "https://help.openai.com/en/articles/4936850-where-do-i-find-my-secret-api-key"

Requirements:
1. Open the python files and set the required paths for files. There are not much things to set.
2. You need to have an OpenAI key for this to work. Open the files and add the key where they are required. There is main.py and Converting_pages.json_to_pages_with_embeddings.py files requiring OpenAI Api key.

Required Libraries:
Tested on python 3.11 on windows.
Libraries to install.
1. json
2. tqdm
3. openai
4. os
5. Numpy
6. Pandas
7. pyarrow
8. pdfplumber
9. sys
x. collections
Don't need a virtual environment just install the libraries for your interpretor wether its pycharm or cmd


**Step 1:** 
Selecting the Data Source
- In this initial step, we have chosen a well-known book as our dataset, specifically "Rich Dad and Poor Dad.pdf".
- In my case its given in that repository. You can use that for testing or can have your own book.

**Step 2:** 
Converting PDF to Text
- To work with the dataset, we begin by converting the "Rich Dad and Poor Dad.pdf" file into a text file. You can use an online tool or do it manually by a small code. It's not a problem.   

**Step 3:** 
Cleaning the Text or Preprocessing Dataset.
- The converted text file may contain irrelevant information or text that we don't need. Remove unnecessary data from start. (Mostly it will be from starting and then it will be smooth. Must see my "rich-dad-poor-dad.txt" document for this part. it will help. In this step, we clean up the text   file by removing such unnecessary content.The standard   preprocessing techniques like tokenization,stemming or lemmatization etc were not required for this project. 

**Step 4:** 
Converting Text to JSON
- We transform the cleaned text file into a structured JSON file. This JSON file will contain information about chapters, pages, and page numbers. Both the conversion code and the resulting JSON file can be found in the provided folder.
- Conversion filename-->"Converting_text_file_to_json_file"
- Resulting json file name--> "pages.json"

**Step 5:** 
Creating Embedded JSON
- In this step, we convert the previously generated "pages.json" file into an embedded JSON file. This file, named "pages_with_embeddings," will include embeddings for the JSON data. The folder contains both the conversion code and the resulting embedded JSON file.
- Conversion file name--> "Converting_pages.json_to_pages_with_embeddings.py"
- Converted filename--> "pages_with_embeddings"

**Step 7:** 
Generating a Parquet File
- Now, we are preparing a Parquet file to store the embedded data. The Parquet file is named "embedded_data," and the code for creating it is provided in the folder.
-Conversion filename--> "Converting_pages_with_embeddings_to_parquett_file.py"
-Converted filename--> "embedded_data.parquett"

**Step 8:** 
Running the Program
- To interact with the dataset and retrieve information, you can run the "main.py" file using a simple python IDE, or you can use CLI for this.

Feel free to ask questions

