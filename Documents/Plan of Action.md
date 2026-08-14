# Plan of Action

This project will use three publicly available CMS hospital quality datasets to explore how Generative AI can transform structured healthcare performance data into clear, audience-specific narratives. The datasets will be cleaned, standardized, analyzed, and converted into structured factual evidence that can be provided to a Large Language Model (LLM).

Rather than training separate models for different audiences, the project will use **prompt engineering and audience-specific evidence selection** to control how the same underlying hospital performance information is communicated. The primary focus is evaluating whether different prompting strategies can change communication style while maintaining factual consistency.

The project workflow is:

**Data Collection → Data Preprocessing → Exploratory Analysis → Factual Narrative Generation → Evidence Selection → Prompt Engineering → LLM Generation → Evaluation → Application**

1. **Dataset Collection**

   * Collect three publicly available CMS hospital quality datasets:

     * Patient Survey (HCAHPS)
     * Healthcare-Associated Infections
     * Timely and Effective Care

2. **Data Preprocessing**

   * Clean and standardize the datasets using Python, pandas, and NumPy.
   * Address missing values, duplicate records, inconsistent formatting, and data types.
   * Select relevant hospital performance measures.
   * Use **Facility ID** to associate performance measures with individual hospitals.

3. **Exploratory Data Analysis**

   * Examine distributions, trends, outliers, and hospital performance patterns.
   * Identify measures that provide meaningful information for narrative generation.

4. **Factual Narrative Generation**

   * Convert structured CMS measures into standardized factual narratives.
   * Preserve important values, comparisons, and performance information from the source data.
   * Create an evidence repository that can be used as grounded context for subsequent text generation.

5. **Audience-Specific Evidence Selection**

   * Select evidence relevant to the requested hospital and communication style.
   * Control which measures are provided to the LLM based on the information needs of each audience.
   * Use the selected evidence as factual grounding for narrative generation.

6. **Prompt Engineering**

   * Develop prompts for four communication styles:

     * Patient Friendly
     * Executive Summary
     * Clinical
     * Community Report
   * Define the appropriate tone, terminology, detail, and technical complexity for each style.
   * Evaluate multiple prompt versions to determine how prompt design affects generated narratives.

7. **Large Language Model Generation**

   * Provide the factual evidence and communication instructions to an LLM.
   * Generate audience-specific hospital performance narratives.
   * Maintain the same underlying evidence while varying how the information is communicated.

8. **Evaluation**

   * Compare generated narratives against the factual source narratives using quantitative and qualitative measures.
   * Evaluate characteristics including:

     * Semantic similarity
     * Content coverage
     * Readability
     * Factual consistency
     * Audience appropriateness
   * Compare results across communication styles and prompt versions to identify the most effective prompting strategies.

9. **Application**

   * Develop a simple user interface demonstrating the completed workflow.
   * Allow users to select a hospital and communication style.
   * Retrieve the appropriate evidence and generate a customized hospital performance narrative.

# Updates from Milestone 1

Since Milestone 1, the project has evolved from a traditional Transformer-based summarization approach toward a **prompt-driven Generative AI architecture grounded in structured hospital evidence**.

The original proposal considered models such as BART and FLAN-T5 and later explored a Retrieval-Augmented Generation (RAG) approach. As development progressed, the methodology was refined to focus on structured evidence selection and prompt engineering rather than requiring separate fine-tuned models or a traditional vector-database retrieval system.

This change better supports the project's primary research objective: determining whether the **same factual hospital performance information can be communicated effectively to different audiences through prompt engineering while preserving factual meaning**.

The final methodology is:

**CMS Data → Preprocessing → Exploratory Analysis → Factual Evidence → Audience-Specific Evidence Selection → Prompt Engineering → LLM Generation → Evaluation → Application**

This approach allows the project to focus on the effect of **prompt design and communication style** while keeping the underlying hospital performance evidence controlled and consistent.
