# task_1_and_task_2

## How to run the tasks in local machine
step 1. pull the github repository using below code  
git pull https://github.com/hasan-moni-321/task_1_and_task_2.git  

step 2. create and activate virtual environment using below code (in Lunux(ubuntu) OS)  
python3 -m venv venv_name    
source venv_name/bin/activate    

step 3. install dependencies/libraries in the virtual environment using below code    
pip install -r requirements.txt    

step 4. create a .env file in the main project folder using below code (linux command)    
touch .env    

step 5. write simple code in .env file for openai_api_key. replace your_openai_api_key with your actual openai api key.    
OPENAI_API_KEY="your_openai_api_key"    

## How to run task 1    
run each cell one by one from top to bottom  

## How to run task 2    
run each cell one by one from top to bottom  

## Technology I used for this application
1. pdfplumber (for reading table based pdf data)
2. pypdf (very smooth for LangChain based applicaton for pdf data reading)
3. LangChain
4. LangGraph
5. StateGraph
6. RAG and Agent
7. RecursiveCharacterTextSplitter
8. OpenAIEmbeddings
9. FAISS
10. retriever
11. gpt-4o model from openAI

## Different technique for summarization  
1. Text Summarization Using Langchain
2. Prompt Templates Text Summarization
3. StuffDocumentChain Text Summarization
4. Summarizing Large Documents Using Map Reduce
5. Map Reduce With Custom Prompts
6. RefineChain For Summarization

## How to improve accuracy for summarization  
1. Preprocessing the input text
   * Clean & normalize: Remove OCR noise, weird symbols, duplicate spaces, etc.
   * Split logically: Break long documents into semantically coherent chunks (e.g., by paragraphs, sections) to avoid context loss.
   * Preserve structure: Keep headings, bullet points, and metadata if they’re important for meaning.
   * Remove irrelevant sections (like disclaimers or repeated boilerplate).
   
2. Prompt Engineering
   * Set clear instructions: Tell the model exactly what kind of summary you want — short/long, factual, in bullet points, with no         opinions, etc.
   * Explicit constraints: For accuracy, say:
     "Summarize the text in 5 bullet points, only using facts from the text.
     Do not add extra information."
   * Role priming:
     “You are a professional technical summarizer who only extracts key facts without interpretation.”
   * Include examples: Few-shot prompting helps the model learn your preferred style.
   * Multi-step prompting: First extract key points, then condense them.

3. Using Retrieval-Augmented Generation(RAG)
   * Store your documents in a vector database (e.g., FAISS, Pinecone, Weaviate).
   * Retrieve only the most relevant parts before summarization.
   * This reduces hallucination by limiting the model’s input to contextually relevant data.
   
4. Model and Parameter choise
   * Bigger ≠ always better: Try models tuned for summarization (e.g., OpenAI gpt-4o-mini, Anthropic Claude 3, Llama 3-Instruct,           Flan-     T5 XXL).
   * Temperature: Lower values (0.0–0.3) make the model more deterministic and factual.
   * Max tokens: Give enough output space so the summary doesn’t cut off.
   
5. Post-processing and verification
   * Fact-checking loop: After generating the summary, re-prompt the model:
       “Verify the following summary against the source text. Mark any incorrect or unsupported statements.”
       Compare multiple outputs: Generate 2–3 summaries and merge consistent points.
   * Named entity consistency check: Ensure names, numbers, and dates match the source.
6. Advanced Techniques
   * Chain-of-Thought Summarization: First extract facts → then compress into a summary.
   * Map-Reduce Summarization:
       * Map: Summarize each chunk individually.
       * Reduce: Summarize the summaries into a final version.
   * Fine-tuning / LoRA adapters: Train the model on examples of your ideal summaries.
   * Evaluation with ROUGE/BERTScore: Measure overlap with reference summaries.


## Limitations
1. Time: Due to time limitations I haven't did the modular coding and Deep R&D.
     1.1 Components
     1.2 Config
     1.3 Constants
     1.4 Entity
     1.5 Exception handling
     1.6 Logging
     1.7 Pipeline
     1.8 utils
   
