# AI-IOWA-MAKE-RAG-BETTER

Repo that shows a few approachable techniques to improving your document retrieval results

## Areas to tweak in RAG Flows

See the diagram [here](./RAG%20Diagram.drawio) to see where some of these fall in the standard RAG process. But most changes that can be made fall into 1 of 3 categories

1. Document Indexing/Preparation
    - The process of getting documents from your source, chunking, cleaning, parsing for metadata, and really transforming in any way before creating your embedding.
2. Document Retrieval
    - The process of finding the most similar indexed documents to you query. This is typically where many apps struggle.
3. Inference
    - After you have already found the document chunks you are intending to reference, this is the process of sending the user query, documents, and any other information to the LLM to generate your answer.

## Running the code

Before running anything in [main.ipynb](./main.ipynb)

1. Create a python virtual environment
2. Run `docker compose up` to create our postgres container
3. Create a `.env` file in the base of this repository that sets `COHERE_API_KEY` to be equal to your api key


## The Data

This uses a snapshot of data pulled from Kaggle with around 15000 movie titles and plots.  The data was pulled verbatim, so no cleaning has been done on it, either for quality or appropriateness.  If you find data you don't think is appropriate, feel free to remove it!