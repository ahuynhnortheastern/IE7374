#######################################################################
# Plan of Action

This system will utilize three publicly available CMS datasets which will be cleaned, combined, and analyzed to uncover meaningful trends and performance insights. Rather than relying on traditional Transformer-based sequence-to-sequence models, the project will leverage a pretrained Large Language Model (LLM), Llama 3 and GPT-4o, combined with Retrieval-Augmented Generation (RAG). This approach allows the model to retrieve relevant statistical findings before generating text fit for different audiences through prompt engineering. This will alleviate the need to have separate models and focus on the dependent variable being the prompts.

The project will begin by collecting, cleaning, and preprocessing the CMS datasets, followed by exploratory data analysis and statistical analysis to identify key trends, relationships, and performance metrics. Next, the Retrieval-Augmented Generation (RAG) pipeline will be developed by generating embeddings from the statistical insights, storing them within a vector database, retrieving the most relevant context, and combining that information with carefully designed prompts for the LLM. Different prompting strategies and communication styles will be evaluated using ROUGE, BLEU, and BERTScore, along with qualitative assessments (i.e. readability, factual consistency, fluency, and audience appropriateness). Finally, a simple user interface will be developed to allow users to upload CMS datasets and automatically generate customized summaries, demonstrating the power of Generative AI tools that can transform structured healthcare data into meaningful, actionable insights for a wide range of users. 

1.	Dataset Collection
    a.	Select and download the following CMS hospital quality datasets:
        •	Patient Survey (HCAHPS)
        •	Healthcare-Associated Infections
        •	Timely and Effective Care
2.	Preprocess Dataset
    a.	Cleaning the dataset using pandas and NumPy
        i.	Address missing values, duplicate rows, formatting, and etc. via   imputation methods
        ii.	Select relevant features
        iii.	If necessary, standardize features
    b.	Merge the datasets using the primary key “Facility ID”
3.	Exploratory Data Analysis
    a.	Uncover dataset insights like trends, outliers, correlations, and distributions
4.	Statistical Analysis
    a.	Generate key performance indicators and summary statistics
    b.	Convert the findings into structured text that can be retrieved by a language model
5.	Retrieval-Augmented Generation (RAG)
    a.	Generate embedding for the findings using a sentence embedding model
    b.	Store the embeddings within a vector database
    c.	Only pull the most relevant information and insight based on the end-users’ prompt
6.	Prompt Engineering
    a.	Create prompt templates for the three audience types: executives, clinical providers, and non-technical users
    b.	Define the communication style, tone, and level of technical understanding for each audience
    c.	Package the retrieved statistical insights with the selected prompt template to feed into the Large Language Model
7.	Large Language Model (LLM) Generation
    a.	Use a pre-trained large language model (i.e. Llama 3 or GPT-4o)
    b.	Generate audience-specific summaries using the pulled insights and prompt template
    c.	Try zero-shot and few-shot prompting to evaluate effect on summary quality
8.	Model Evaluation
    a.	Assess performance of generated summaries using the following metrics:
        i.	BLEU (Similarity)
        ii.	ROUGE (Context Coverage)
        iii.	BERTScore (Semantic Similarity)
    b.	Perform a quality check for the following:
        i.	Readability
        ii.	Factual consistency
        iii.	Audience appropriateness
    c.	Compare the performance and quality of the different prompts and audiences
9.	Deployment
    a.	Develop a user interface for uploading CMS data
    b.	Allow users to select their preferred communication style
    c.	Generate custom AI summaries 

#######################################################################
# Updates from Milestone 1

Between Milestone 1 and 2, the project will be evolving from a transformer-based text summarization to a Retrieval-Augmented Generation based model. The original proposal focused on leveraging Transformers such as BART or FLAN-T5, to generate summaries but moving forward the project will now adopt a RAG-centric architecture which will be supported by a more modern Large Language Model (i.e. Llama 3 or GPT-4o). The benefits of using a more modern LLM like Llama 3 or GPT-4o instead of a Transformer-based model is due to RAG’s flexibility without the need for extensive fine-tuning.
In addition, the methodology was updated to the following: 
Data Preprocessing to Exploratory and Statistical Analysis to Embedding Generation to Retrieval to Prompt Engineering to Text Generation (Using LLMs) to Evaluation

#########################################################################