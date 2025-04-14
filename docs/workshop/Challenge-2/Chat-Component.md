# Chat Component

The Chat component integrates seamlessly with the backend to provide a robust and dynamic chat experience. It supports:

## General Chat:
    - The greeting function handles general queries and greetings.
    - It uses Azure OpenAI to generate responses, either via the AIProjectClient or directly using the openai library.


## SQL Query Generation:
    - The get_SQL_Response function dynamically generates SQL queries based on user input.
    - It uses Azure OpenAI to create the SQL query and executes it against the database using the execute_sql_query function.
 

## Azure Cognitive Search:
    - The get_answers_from_calltranscripts function retrieves answers from indexed call transcripts using Azure Cognitive Search.
    - It uses a hybrid query approach (vector_simple_hybrid) to combine semantic and vector-based search.


## Chart Data Generation:
    - The process_rag_response function in chat_helper.py dynamically generates chart data from RAG responses.
    - It uses Azure OpenAI to process the RAG response and generate valid JSON data compatible with Chart.js.

       

