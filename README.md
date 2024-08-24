# End-to-End-RAG-using-Amazon-Bedrock

# How to run?

# 1. Create a new Environment
 
''' conda create -n llmapp python=3.8 -y '''

# 2. Activate the environment

'''conda activate llmapp'''

# 3. Install the requirement package

# RAG Architecure
PDF Documents->Extract Data -> Chunking -> Embedding Model-> Convert Text to vector Embedding -> Knowledgebase:
(Store in vector database)

If user is sending the query to knowledgebase, this particular knowledge base return rank results based on k parameter let's say k=3
then have connect to LLM now rank result go to LLM and particular query LLm try to understand and preapre the correct results and send the result to LLM.

Query to Knowledge Base:

1. A user inputs a query into the system.
The knowledge base processes this query and retrieves the top k results, with k=3 as per your example. This means it returns the three most relevant documents or entries based on the content of the knowledge base.
Connecting to LLM:

2. These top k results from the knowledge base are then passed to a Large Language Model.
The LLM uses these results as contextual information. It understands and analyzes the content of these top results to generate a more accurate and contextually enriched response.
Using RAG Architecture:

3. Retrieval-Augmented Generation (RAG) combines the benefits of retrieval-based and generative approaches. In this setup, the LLM (like a variant of GPT or a specialized model) uses the retrieved documents to inform its generation process.
The RAG model fetches context from the knowledge base (the top k results) and uses this context to generate a response. This process ensures that the output is not only relevant but also deeply grounded in the retrieved documents.
Generating and Sending Results:

4. The LLM, augmented by the RAG approach, synthesizes the information from the top results and the original query to produce a comprehensive and accurate answer.
This final result is then sent back to the user, providing a response that is not only tailored to the query but also enriched by the specific information extracted from the best-matching knowledge base entries.
Feedback Loop (optional but beneficial):

5. Feedback from the user's satisfaction with the response could be utilized to further train and refine the models, enhancing accuracy and relevance for future queries.