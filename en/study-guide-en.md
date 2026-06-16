# AWS Certified AI Practitioner AIF-C01

# Exam

## Candidate Profile and Requirements

- **Entry Level:** This is a **Foundational** level certification, meaning it is designed for individuals who want to demonstrate a basic understanding of AI and AWS tools, without the need for deep experience.
- **Recommended Experience:** It is suggested to have up to 6 months of exposure to AI and ML technologies on AWS. Although not mandatory, it is recommended to first obtain the Cloud Practitioner certification, as many of those infrastructure concepts are taken for granted.
- **What you DO NOT need:** The exam does not require you to know how to program algorithms, perform complex mathematical analysis, advanced data engineering, or technical diagramming. The focus is on using managed services, not developing code from scratch.

## Exam Structure and Logistics

- **Format:** It consists of 65 questions in total: 50 are scored and 15 are experimental.
- **Question Types:** Includes multiple choice, multiple response, ordering, matching, and case studies.
- **Time and Cost:** You will have 90 minutes to complete the exam, which costs $100 USD.
- **Passing Score:** You must score at least 700 out of a maximum of 1,000 points.

## Content Domains

The exam is divided into five main areas, highlighting that **more than half of the exam focuses on generative AI.**

1. **Foundations of AI and ML (20%):** Basic concepts, types of learning (supervised, unsupervised, reinforcement), and ML lifecycle.
2. **Foundations of Generative AI (24%):** GenAI concepts, transformers, and multimodal models.
3. **Applications of Foundation Models (28%):** Prompt engineering, continuous training, and RAG.
4. **Guidelines for Responsible AI (14%):** Bias, fairness, explainability, and transparency.
5. **Security, Compliance, and Governance (14%):** Protection of AI systems and AWS regulations.

## Key AWS Tools

You should familiarize yourself with the use cases of the following main services:

- **Amazon SageMaker:** To build, train, and deploy models.
- **Amazon Bedrock:** To work with foundation models and generative AI.
- **Specific AI Services:** Comprehend, Rekognition, Transcribe, Polly, and Lex.

## Study Tips

- **Preparation Time:** It is estimated that a beginner needs about 20 hours of study, while someone with experience might require only 5 hours.
- **Association Strategy:** An effective technique is to create flashcards to associate each AWS service with its primary function.

# Study Book

## **AI and ML Basics**

### **Basic AI Terminology and Concepts**

#### Fundamental Definitions

- **Artificial Intelligence (AI):** A broad field that seeks to create computer systems with human-like problem-solving capabilities. Its goal is to **simulate** human intelligence to perform tasks such as recognizing images, writing poems, or making decisions.
- **Machine Learning (ML):** A subset of AI that gives computers the ability to learn from data without being explicitly programmed for each step. ML algorithms identify patterns in data to make predictions or classifications.
- **Deep Learning:** An advanced evolution of ML that uses artificial neural networks with multiple layers to process complex data such as audio, images, and natural language.

#### Components and Specific Technologies

- **Neural Networks:** Computational models inspired by the structure of the human brain, composed of interconnected nodes organized in layers: input, hidden, and output. The connections between these neurons have numerical weights that the model adjusts to learn patterns.
- **Computer Vision:** The field of AI that allows machines to **see** and interpret visual information from the real world. The key service in AWS for this is **Amazon Rekognition,** which identifies objects, people, scenes, and activities in images and videos.
- **Natural Language Processing (NLP):** Technology that allows computers to understand, interpret, and generate human language, whether text or speech. It is used in chatbots, translation, and sentiment analysis. AWS offers services such as:
    - **Amazon Comprehend:** Information extraction
    - **Amazon Translate:** Translation
    - **Amazon Lex:** Chatbots

#### Training and Inference

- **Training:** The phase where the algorithm is fed with historical data so it learns to detect patterns. A best practice is to split the data into training, validation, and test groups.
- **Inference:** The act of using the already trained model to request and obtain a prediction based on new data. There are two main types:
    - **Real-time:** Instantaneous responses, like a chatbot.
    - **Batch:** Processes large groups of data all at once, ideal for reports.

#### Bias and Fairness

- **Bias:** Occurs when an AI system unfairly favors a group or individual, usually because the training data was unbalanced or incomplete.
- **Fairness:** The ethical principle of ensuring that AI systems make impartial decisions and do not discriminate based on attributes such as race, gender, or socioeconomic status.
- **AWS Tools: Amazon SageMaker Clarify** is the service designed to detect bias in data and models, as well as provide explainability on how the model makes its decisions.

### Types of Learning

#### Supervised Learning

It is the type of learning where the model is trained using **labeled data,** meaning that each data input is accompanied by the correct answer. It can be compared to a student learning under the guidance of a teacher.

This is divided into two main tasks:

- **Classification:** The goal is to assign data to **predefined categories or classes**. The model identifies patterns to label new examples into discrete groups.
    - Examples: Spam email detection (yes/no), medical diagnosis, image recognition, and credit risk assessment (low/high).
- **Regression:** Used to **predict continuous numerical values** instead of categories. It analyzes the relationship between variables to make forecasts.
    - Examples: Predicting home prices, stock market trends, calculating life expectancy, or temperature forecasts.

#### Unsupervised Learning

In this method, the model is trained with **unlabeled data**. There is no prior "correct answer"; the algorithm must discover hidden patterns, structures, or relationships within the data on its own.

Its main approaches are:

- **Clustering:** Groups data points based on their similarities using distance measurement techniques.
    - Example: Segmenting customers by purchasing habits for personalized marketing.
- **Dimensionality Reduction:** The process of reducing the number of input variables in a dataset while keeping the essential information. This helps combat the curse of dimensionality and prevents overfitting.
- **Association:** Looks for rules that describe large portions of data, such as relationships between variables.
    - Example: If a customer buys bread, they are likely to buy butter.

#### Reinforcement Learning

This type of learning is not based on static data, but on an agent interacting with an environment. The agent learns through a process of trial and error, receiving rewards for correct actions and punishments for incorrect ones.

- **Mechanisms:** The agent's goal is to maximize the total reward accumulated over time. It is similar to how a human learns to ride a bicycle.
- **Use Cases:** Video games, robot navigation, and autonomous vehicles that must decide in real time how to steer or brake.
- **AWS Highlight:** The **AWS DeepRacer** service uses reinforcement learning to train autonomous racing cars in a 3D simulator.

| **Learning Type** | **Data** | **Main Objective** | **Key Concept** |
| --- | --- | --- | --- |
| **Supervised** | Labeled | Predict categories or numbers | Guide/Teacher |
| **Unsupervised** | Unlabeled | Find structures or reduce data | Explorer/Independent |
| **Reinforcement** | No prior data | Learn optimal decisions | Reward/Punishment |

### Data Types in AI

#### Labeled vs. Unlabeled Data

- **Labeled data:** Data samples that already include the correct answer or description (e.g., emails marked as "spam" or "not spam"). This data is the prerequisite for supervised learning. In AWS, the service designed for humans to identify raw data and add informative labels is **Amazon SageMaker Ground Truth.**
- **Unlabeled data:** Consists of raw data that lacks predefined labels, categories, or tags. It is used in unsupervised learning so the model can discover structures, patterns, or groupings on its own.

#### Structured vs. Unstructured Data

- **Structured data:** Information organized in a predefined format, typically rows and columns within a spreadsheet or database. For the exam, mentally associate the concept of tables and structured data with the **Amazon Redshift** service.
- **Unstructured data:** Data that does not have a fixed format or structure, making it difficult to analyze with traditional methods. Key examples include images, text, audio, and video. To process them effectively, advanced AI techniques like NLP or Computer Vision are required.

#### Specific Data Types and their AWS Services

- **Text:** Classified as unstructured data. The AWS service for analyzing text, extracting insights, and detecting sentiments is **Amazon Comprehend.**
- **Images:** Unstructured data that requires computer vision to be interpreted. You should associate images and video with the **Amazon Rekognition** service, which identifies objects, people, and scenes.
- **Time series:** Values collected continuously over time, such as stock prices or hourly temperature. The critical mental note for the exam is to associate trend prediction in time series with **Amazon Forecast.**
- **Scanned documents:** Although they contain text and images, their data extraction is performed with **Amazon Textract.**

### **ML Development Lifecycle**

#### Data Collection

- **Purpose:** Gather relevant, high-quality data from various sources so the model can learn patterns.
- **Key Services:** Storage services like **Amazon S3** are used to centralize information, **AWS Glue** for integration, and **AWS Data Lake** to manage large volumes of data from multiple sources.
- **Labeling:** If the data does not have labels, **SageMaker Ground Truth** is used for humans to add the informative descriptions required for supervised learning.

#### Exploratory Data Analysis (EDA)

- **Purpose:** Investigate the dataset to discover structures, detect anomalies, and visualize patterns using statistics and charts.
- **Tools:** **SageMaker Notebook Instances** or **SageMaker Studio** are used, which come with pre-installed Python libraries like Pandas and Matplotlib for analysis.

#### Data Processing

- **Purpose:** Clean raw data, which is often "dirty" (missing values, duplicates, errors, or inconsistencies), and normalize it to make it valuable for the model.
- **Quick Association:** The main service is **Amazon SageMaker Data Wrangler**, which offers more than 300 built-in transformations to automate this process without writing complex code.

#### Feature Engineering

- **Purpose:** Select, create, or transform input variables to significantly improve the model's performance and predictive capability.
- **Storage:** **SageMaker Feature Store** is used, a centralized repository to store, share, and reuse features across different ML projects.

#### Training and Hyperparameter Tuning

- **Training:** Consists of feeding the algorithm with historical data (usually 70-80% of the total dataset) so it learns patterns.
- **Hyperparameter Tuning:** Hyperparameters are external configurations (such as **learning rate, batch size, or epochs**) that must be defined before training to control how the model learns.
- **Optimization: SageMaker Automatic Model Tuning** runs multiple training jobs testing different ranges of hyperparameters to find the best-performing version.

#### Evaluation

- **Purpose:** Determine model accuracy using data it did not see during training to ensure it generalizes well to the real world.
- **Critical Metrics:**
    - **Classification:**
        - Accuracy
        - Precision
        - Recall
        - F1 Score
    - **Regression:**
        - Mean Squared Error (MSE)
        - Root Mean Squared Error (RMSE)
    - **Generative:**
        - ROUGE
        - BLEU
        - BERTScore

#### Deployment

- **Purpose:** Publish the trained model as an endpoint so applications can query it.
- **Inference Modes:**
    - Real-time: For instant responses.
    - Batch: Processes large groups of data asynchronously when an immediate response is not critical.

#### Monitoring

- **Purpose:** Watch the model's performance in production to detect **Drift**, which occurs when the model loses accuracy over time due to changes in real-world data.
- **Key Service: Amazon SageMaker Model Monitor** automatically detects data drift, quality drift, and bias, issuing alerts to decide if the model needs to be retrained.

### Performance and Business Metrics

#### Model Performance Metrics

**Classification (Critical Metrics)**

- **Accuracy:** Calculated as the number of correct predictions divided by the total number of predictions.
    - **Note:** Can be misleading if the dataset is unbalanced. A model could have high accuracy simply by always predicting the most frequent class, ignoring the minority class.
- **Precision:** Measures the quality of positive predictions. Answers: *"Of all the cases the model marked as positive, how many actually were?"* It is vital when the cost of a **false positive** is high (e.g., marking a legitimate email as spam).
- **Recall (Sensitivity):** Measures the number of positive cases the model is able to identify. Answers: *"Of all the actual positive cases, how many did the model manage to catch?"* It is critical when we cannot afford **false negatives** (e.g., detecting a disease).
- **F1 Score:** The harmonic mean between precision and recall.
    - **Use:** Used primarily when there is an uneven class distribution or when looking for a healthy balance between avoiding false positives and false negatives.
- **AUC (Area Under the Curve):** Represents the probability that the model ranks a random positive example higher than a random negative example.
    - **Interpretation:** A value of **1.0** indicates perfect performance, while **0.5** means the model is no better than random guessing.

**Regression (Critical Metrics)**

- **Mean Squared Error (MSE):** Average of the squared errors (difference between the actual and predicted value).
    - **Characteristics:** By squaring, it penalizes larger errors (outliers) much more than smaller ones.
- **Root Mean Squared Error (RMSE):** The square root of the MSE.
    - **Advantage:** Expresses the error in the same units as the variable we are predicting (e.g., dollars, meters, degrees), making it much easier for the business to interpret.

#### Business Metrics

- **ROI (Return on Investment):** Measures the economic profitability of the project. It compares the financial benefits generated (savings or extra earnings) against the total investment in development, infrastructure, and deployment of the model.
- **Customer Satisfaction:** Evaluates the direct impact of the AI solution on the end-user experience:
    - **NPS (Net Promoter Score):** A scale from 0 to 10 that measures customer loyalty based on how likely they are to recommend the product.
    - **Sentiment Analysis:** AWS suggests using **Amazon Comprehend** to automatically categorize comments as positive, negative, neutral, or mixed. It serves as a real-time indicator of user satisfaction.
- **Operational and Cost Metrics:**
    - **Development costs:** Initial investment in human talent and data acquisition.
    - **Cost per user:** Infrastructure cost (cloud/inference) generated by each active user when interacting with the model.
    - **General opinion:** Qualitative feedback collected from direct interviews or surveys to understand the perceived value.

## **Generative AI Basics**

### **Technical Foundations of GenAI**

#### Tokens

- **Definition:** The **basic unit** of data processed by natural language processing and generative AI models.
- **Scale:** A token can represent a whole word, a part of a word, a punctuation mark, or even a single character.
- **Internal Vocabulary:** During their training, models create an internal vocabulary of tokens; larger models typically handle between 30k and 100k tokens.
- **Capacity and Cost:** Each token consumes memory and computing power. In services like Amazon Bedrock, the cost is frequently based on the number of tokens processed (input) and generated (output).

#### Chunking

- **Definition:** The process of dividing large volumes of text or data into smaller, more manageable pieces.
- **Purpose:** Essential because models have a limit on the amount of information they can process at one time, known as the **context window**.
- **Application in RAG:** Before converting data into numerical representations, the dataset is chunked so the model can retrieve relevant information efficiently.
- **Risks:** Inadequate chunking can cause the model to lose context or the relationship between parts of the text.

#### Embeddings

- **Definition:** Vector representations that capture the semantic meaning and relationships between data.
- **Operation:** They allow the model to analyze patterns mathematically; for example, words with similar meanings will have close numerical representations in the vector space.
- **Creation:** They are generated by specialized ML models and serve as a kind of external memory for the system.

#### Vectors

- **Definition:** In this context, a vector is a string of numbers where each position represents a feature or direction in a mathematical space.
- **Vector Space:** The multidimensional mathematical structure where these vectors exist.
- **Relationship:** The distance between vectors within this space correlates with the relationship between the data they represent.

#### Latent Space

- **Concept:** A compressed mathematical representation of data where the model captures the essential features and patterns.

### Model Architecture

#### Foundation Models

- **Definition:** These are **general-purpose** models trained on massive amounts of data from diverse sources.
- **Pre-training:** They are considered "pre-trained" models because they can be adapted or refined using **fine-tuning** to perform domain-specific tasks.
- **Scale:** Involves a massive scale of parameters (internal values that the model adjusts) and terabytes of data.
- **Main Types:** Large Language Models (LLMs) and multimodal models are the two main categories.

#### LLMs based on Transformers

- **Relationship to FMs:** An LLM is a type of foundation model that specifically implements the **Transformer architecture.**
- **Operation:** Its primary task is to predict the next word in a sequence based on grammatical patterns, style, and tone.
- **Key Innovations:**
    - **Multi-head attention:** Allows the model to consider all parts of the input simultaneously and understand context in long passages.
    - **Positional encoding:** Reorders words that fall out of sequence after applying attention, allowing the model to process data in parallel rather than just sequentially.
- **Structure:**
    - **Encoder:** Analyzes the input sequence to extract contextually meaningful representations.
    - **Decoder:** Generates the output text word by word based on what was learned from the encoder.

#### Diffusion Models

Diffusion models are a class of generative models that learn to create data (usually images) through a process of **destruction and reconstruction**. Unlike other models that try to copy data, these learn to "clean" noise to reveal a coherent image.

- **Use:** They are the main technology for generating realistic images and audio.
- The training of a diffusion model consists of two main stages:
    - **Forward Diffusion**
        
        In this stage, the model takes a real image and gradually adds "Gaussian noise" (random dots) over a series of steps.
        
        - At the end of this process, the original image is completely unrecognizable; it becomes pure random noise.
        - The model observes this process to mathematically understand how information degrades.
    - **Reverse Diffusion / Denoising**
        
        Here is where the "magic" happens. The model learns to perform the opposite process: **remove noise step by step**.
        
        - It is trained to predict how much noise was added in each step and how to subtract it.
        - At the end, starting from a block of random noise, the model can "sculpt" a sharp image that never existed before.

#### Multimodal Models

- **Capability:** These models can understand and generate different types of content simultaneously, such as **text, images, audio, and video.**
- **Architecture:** They generally use a combination of transformer and diffusion models to handle different data modalities.

#### Other Models

- **GAN:** They use two neural networks that compete against each other (generator and discriminator) in a game-like setting to produce realistic content.
- **VAE:** They use a probabilistic system to map input data to a distribution and then reconstruct similar data from samples of that distribution.

### **Foundation Model Lifecycle**

#### Data Selection

- **Massive Scale:** Datasets for training FMs are huge; for example, models like GPT-4 process around 45 terabytes of data.
- **Common Sources:** Data comes from web page crawls (WebText), Wikipedia, and large collections of public domain books.
- **Quality and Diversity:** It is essential for data to be high quality and diverse to reduce risks of bias and toxic content.
- **No Prior Labeling:** Unlike traditional ML, this stage does not require exhaustive data cleaning or labeling, as the model works seamlessly with unlabeled data.
- **Specialized Methods:** Frameworks like DSIR (Data Selection with Importance Resampling) are used to filter the most relevant information for specific applications.

#### Pre-training

- **Semi-supervised Learning:** The model uses this technique to create synthetic labels based on the data itself, such as predicting missing words in a sentence.
- **Objective:** In this phase, the model develops the ability to understand and generate human-like text.
- **Continuous Pre-training:** There is the concept of continuous pre-training, where the model is constantly exposed to new data to refine what it has learned.
- **Technical Infrastructure:** Requires a massive amount of compute, primarily using GPUs for parallel processing or specialized TPUs for ML tasks.

#### Fine-tuning

- **Customization:** Consists of retraining an existing model with a smaller, specialized, and labeled dataset for specific tasks (e.g., customer support or legal topics).
- **Main Types:**
    - **Instruction Fine-Tuning:** Examples of how the model should respond to specific prompts are provided.
    - **RLHF (Reinforcement Learning from Human Feedback):** Aligns model responses with human values and preferences using a reward and punishment system based on human judgment.
- **Parameter Efficiency (PEFT):** Methods like LoRA allow updating only a small group of parameters to save costs and resources.
- **Risks:** Excessive refinement can cause overfitting, making the model lose its general-purpose capability.

#### Evaluation

- **Purpose:** Verify if the model is accurate, if it generates hallucinations, or if it produces harmful content.
- **Evaluation Methods:**
    - **Human Evaluation:** Critical for judging creativity, ethics, and user experience.
    - **Reference Datasets (Benchmarks):** Quantitative evaluations of accuracy, speed, and robustness against agreed standards.
- **Standard Metrics:** You should know **ROUGE** (for summaries), **BLEU** (for machine translations), and **BERTScore** (for semantic evaluation).

#### Feedback and Implementation

- **Implementation:** The model is put into production via an API once it meets performance criteria.
- **Continuous Monitoring:** Metrics for latency, accuracy, and safety (toxic content) must be constantly tracked.
- **Usage Data Collection:** User behavior (such as "liking" or "disliking" in a chat interface) is collected as **feedback** to inform the next version of the model.
- **Update Cycles:** It is common to have minor updates every couple of months and major improvements every six months or a year.

### **Capabilities and Limitations**

#### Advantages of Generative AI

- **Adaptability:** A single Foundation Model can perform tasks across various domains (summarizing, translating, coding, creating content) without needing a specific model for each problem.
- **Responsiveness:** GenAI can generate responses in near real-time, which is fundamental for interactive applications like virtual assistants and chatbots.
- **Simplicity:** Drastically lowers the technological barrier to entry, allowing people without technical knowledge to use advanced AI using natural language.
- **Personalization:** Responses can adapt automatically to user preferences based on prior interactions.
- **Data Efficiency:** A model can learn or adjust using just a few pieces of new information.

#### Disadvantages and Critical Limitations

- **Hallucinations:** Occur when the model generates information that sounds convincing and professional but is false, misleading, or nonsensical. This happens due to the probabilistic nature of the models and the lack of relevant data in their training.
- **Lack of Determinism (Nondeterminism):** Given the exact same prompt, the model may give different answers because it relies on probabilities rather than fixed rules.
    - Note: The Temperature parameter controls this level of randomness or "creativity."
- **Limited Interpretability:** GenAI systems are often considered a black box because, due to their extreme complexity, it is very difficult to understand exactly why the model made a specific decision. This is a major challenge in regulated industries like medicine or finance.
- **Latency:** Larger and more complex models require more mathematical operations per generated token, increasing user wait time. There is a trilemma between reasoning capability, cost, and latency where you cannot maximize all three at the same time.
- **Inaccuracy and Recency:** The model's knowledge is frozen at its training date. If the source data is outdated or contains errors, the model will produce incorrect information.
- **Limited Context Windows:** There is a physical limit to the number of tokens a model can process at once. If the text is too long, the model may suffer from the "lost in the middle" effect, ignoring crucial information located in the center of the input.

#### Mitigation Strategies

- To reduce hallucinations and lack of **recency**: Use RAG (Retrieval-Augmented Generation) to connect the model to external and private sources.
- To improve interpretability: Use SageMaker Model Cards to document design and limitations.
- To control non-determinism: Set Temperature close to 0 if you want consistent, fact-based answers.

### **GenAI Infrastructure on AWS**

#### Amazon Bedrock: The Central Platform

It is the main AWS service for building generative AI applications, defined as "Model as a Service" (MaaS).

- **Purpose:** Allows access to foundation models from leading providers (such as Amazon, Anthropic, Meta, Mistral, Stability AI, and Cohere) through a unified API.
- **Key Features:**
    - **Model Catalog:** A collection of language models (LLMs) and multimodal models (image, audio, video).
    - **Playgrounds:** Environments to test chat, text, and image models without writing code.
    - **Knowledge Bases (RAG):** Connects models with private company data to provide precise answers.
    - **Agents:** Systems that automate multi-step business tasks by invoking APIs.
    - **Guardrails:** Filters to block harmful content or redact sensitive information.
- **Deployment Models:** On-demand (serverless, pay per token processed) and provisioned throughput.
- **Security:** AWS guarantees that customer data is not used to train the base models of third parties.

#### Amazon SageMaker JumpStart: The Technical Catalog

It is a resource center within Amazon SageMaker that offers **pre-trained models and built-in algorithms.**

- **Key Difference:** Unlike Bedrock, JumpStart is designed for technical users who want more control over infrastructure, training, and deployment.
- **Use:** Allows selecting a model, performing fine-tuning for a specific use case, and deploying it on managed compute instances.

#### PartyRock: The No-Code Environment

It is a no-code development environment based on Amazon Bedrock to create AI applications quickly.

- **Features:** It is free, uses multiple models, and allows creating experimental applications using widgets.
- **Profile:** Ideal for rapid prototyping and creative experimentation without needing an AWS account.

#### Amazon Q: The Intelligent Virtual Assistant

It is an assistant based on generative AI designed specifically for work and development, built on Amazon Bedrock. It is divided into two main variants:

- **Amazon Q Business:**
    - **Function:** Helps employees get answers, summarize documents, and generate content based on the company's own data and systems.
    - **Connectivity:** Includes more than 40 connectors to index data from tools like Slack, Microsoft 365, and Salesforce.
- **Amazon Q Developer:**
    - **Function:** Helps developers with coding tasks, debugging, testing, and optimizing AWS resources.
    - **Integration:** Integrated into IDEs and directly in the AWS console to answer technical questions.

| **Service** | **Control Level / User** | **Distinctive Feature** |
| --- | --- | --- |
| **Amazon Bedrock** | Developer / Enterprise | Access to multiple models via a **unified API** (without managing servers). |
| **SageMaker JumpStart** | Technical / Data Scientist | **Maximum control** over deployment and training of open-source models. |
| **PartyRock** | Beginner / Curious | **Free, no-code** application creation for prototypes. |
| **Amazon Q** | Business User / Developer | **Ready-to-use assistant** that understands your company's data or code. |

## **Applications of Foundation Models**

### Design Considerations

#### Cost

- Model cost is calculated primarily based on the **number of tokens** of input and output.
- A common mistake is always choosing the largest model; however, massive models can cost up to 10 times more per token than small models, so you should choose the most economical model that gets the job done.
- Customization strategies like pre-training have an extremely high cost, while techniques like RAG or in-context learning offer much lower costs as they do not modify the internal weights of the model.

#### Modality

- Modality defines the types of data a model can understand and generate, including text, images, audio, and video.
- You should select the modality strictly based on the requirements; using a multimodal model for an application that only requires text is inefficient and unnecessarily increases costs.

#### Latency

- Latency is the delay in response time from the system, which is critical in real-time applications like customer support chatbots.
- Larger models with more parameters typically have higher latency because they perform more mathematical operations per generated token.
- For resource-constrained devices (such as drones or IoT), small language models are recommended to obtain low-latency inference at the edge.

#### Model Complexity (The Trilemma)

- There is a fundamental tension known as the AI trilemma, where it is not possible to simultaneously maximize reasoning capability, latency, and cost.
- A model with greater reasoning capability requires more parameters, which increases both cost and response time.

#### Prompt Caching

- **Prompt caching** is a cost and performance optimization technique that stores the processing of fixed contexts or instructions that repeat across multiple calls in memory.
- If an application uses an extensive *system prompt* (of several thousand tokens) in thousands of daily requests, caching avoids reprocessing those tokens.
- This technique results in a **significant reduction in both latency and operational cost** in applications with reusable context.

#### **Other Relevant Metrics and Limits**

- **Context Window:** Defines how much text the model can process in a single call; if the text is too long, the model may suffer from the **"lost in the middle"** effect, ignoring central information.
- **Output Length:** Limiting the maximum response length helps control cost and improves latency by terminating generation earlier.
- **Efficiency:** It is essential to monitor system performance using metrics like **throughput** (requests per second) and memory usage to ensure scalability.

### Inference Parameters

#### Temperature

Temperature controls the level of randomness or "creativity" in the model's responses.

- **Range:** Generally from 0 to 1.
- **Low values (close to 0):** Make the model more deterministic and predictable. The model will always choose the most probable tokens, which is ideal for fact-based tasks like FAQs, technical instructions, or data extraction.
- **High values (close to 1):** Flatten the probability distribution, allowing less probable tokens to be chosen. This produces more diverse, creative, and varied responses, useful for brainstorming or creative writing.

**Top P (Nucleus Sampling)**

Selects the next token based on a cumulative probability threshold.

- **Operation:** The model sums the probabilities of the most likely words until reaching the defined P value.
- **Effect:** If Top P is set to 0.5, the model will only consider the smallest set of words whose cumulative probability is equal to or greater than 0.5.
- **Impact:** Like temperature, a **higher Top P increases the diversity and creativity of responses.**
- Example:
    
    **The Scenario**
    Imagine the model is deciding which word follows after: *"The sky is..."*
    
    Suppose these are the probabilities the model calculates for the next word:
    
    | **Word** | **Probability** | **Cumulative Probability** |
    | --- | --- | --- |
    | **Blue** | 40% (0.4) | 0.4 |
    | **Cloudy** | 20% (0.2) | **0.6** (Threshold reached) |
    | **Grey** | 15% (0.15) | 0.75 |
    | **Green** | 5% (0.05) | 0.80 |
    
    **Applying Top P = 0.5**
    The model starts adding from the most likely down until reaching 0.5:
    
    1. **Blue (0.4):** Has not reached 0.5 yet. **It stays.**
    2. **Cloudy (0.2):** $0.4 + 0.2 = 0.6$. The 0.5 threshold is passed! **It stays.**
    3. **Grey and Green:** Since the threshold was met with the previous ones, these **are completely discarded**, even though "Grey" has a decent probability.
    
    **Result:** The model will only choose (at random) between **Blue** or **Cloudy**.
    

#### Top K

Limits the number of token options the model considers for generating the next word to the K most probable tokens.

- **Effect:** If K is 2, the model will only choose between the two most likely words, regardless of how high the absolute probability is.
- **Impact:** As the K value increases, so does the diversity and randomness of the output.

#### Parameter Interaction

It is important to know that these parameters interact with each other and can cause unexpected results if they are all adjusted at the same time.

- **AWS Recommendation:** It is suggested to use either Temperature or Top P, but not both simultaneously.
- **Using Top K:** This parameter can be effectively combined with both Temperature and Top P to refine control.

#### Stop Sequences

These are specific words, phrases, or punctuation marks that indicate to the model that it must finish its generation immediately.

- **Practical Example:** If you are generating a JSON object, you can set the character "}" as a stop sequence so the model stops writing once the object structure is closed.
- **Purpose:** They help maintain brevity and prevent the model from generating irrelevant content after completing the task.

#### Output Length

Defines the minimum or maximum size of the response.

- **Impact on Costs and Latency:** Limiting the output length is a key design strategy, as reducing the number of generated tokens decreases inference cost and improves latency.
- **Risk:** If the limit is too low, important content may be truncated.

| **Parameter** | **Primary Function** | **Effect of Increasing the Value** |
| --- | --- | --- |
| **Temperature** | Randomness / Creativity | More creative and less predictable. |
| **Top P** | Cumulative probability threshold | Greater diversity in the chosen vocabulary. |
| **Top K** | Fixed number of likely options | Greater randomness (within the K options). |
| **Output Length** | Response size | Higher cost and latency, but prevents truncation. |
| **Stop Sequence** | Text termination | Controls formatting and avoids extra text. |

### Model Customization

#### Fine-tuning

This technique consists of **retraining the weights or parameters** of a pre-trained model using a smaller, more specific dataset.

- **Data:** Uses **labeled data** (supervised process) so the model learns to perform specific tasks, such as customer support or legal analysis.
- **Main Types:**
    - **Instruction Fine-Tuning:** Processes prompt and response examples so the model learns behavioral patterns.
    - **RLHF (Reinforcement Learning from Human Feedback):** Aligns model responses with human values and preferences using rewards and punishments based on human judgment.
- **Efficient Methods:** Techniques like LoRA (Low-Rank Adaptation) and ReFT allow adjusting only a small percentage of parameters, reducing cost and required resources.
- **Risk:** The main challenge is overfitting, where the model becomes too expert on the new data and loses its general-purpose capability.

#### RAG (Retrieval-Augmented Generation)

Unlike fine-tuning, RAG **does not modify the internal weights** of the model.

- **Operation:** Connects the model to **external data sources** (such as vector databases) at runtime to provide informed and updated answers.
- **Process (Retrieve-Augment-Generate):**
    1. **Retrieve:** Finds relevant fragments using similarity search.
    2. **Augment:** Inserts those fragments as additional context in the original prompt.
    3. **Generate:** The model responds based on the provided information.
- **Key Advantage:** It is the best strategy for reducing hallucinations and handling dynamic or private information.

#### Continued Pre-training

Used to improve the model's general understanding of language and context in a specific domain.

- **Data:** Uses large volumes of raw text or unlabeled data.
- **Use Case:** Ideal when there is a lot of technical literature on a topic but little labeled data for specific tasks.
- **AWS Support:** Amazon Bedrock supports this for select models in the Amazon Titan family.

#### Distillation

The process of transferring knowledge from a large, complex model (teacher) to a smaller, more efficient one (student).

- **Mechanism:** The student learns from the probability distributions produced by the teacher, capturing much of its capability.
- **Advantages:** The result is a model with low latency and lower cost, ideal for deployment on resource-constrained devices like mobile phones or IoT systems.

**Comparison Summary for the Exam:**

| **Technique** | **Does it change model weights?** | **Data Type** | **Primary Use Case** |
| --- | --- | --- | --- |
| **Fine-tuning** | Yes | Labeled | Style, tone, or behavior change. |
| **RAG** | No | External | Private data that changes frequently. |
| **Continued Pre-training** | Yes | Unlabeled | Deep specialization in a domain. |
| **Distillation** | Yes (in the student) | Probabilities | Fast inference on mobile devices. |

### **Vector Databases on AWS**

Vector databases are specialized components designed to efficiently store, manage, and search high-dimensional vector embeddings. These databases are fundamental for Retrieval-Augmented Generation (RAG) systems, as they allow finding similar items by comparing numerical vectors instead of relying solely on exact keyword matches.

#### Amazon OpenSearch Service

- **Main Purpose:** The preferred option for vector search at a massive scale.
- **Technical Capabilities:** Based on the **Apache Lucene** library, it offers full-text search capabilities but stands out as a vector store for its ability to handle millions of documents with **high concurrency and low latency.**
- **Search Types:** Supports vector similarity search, K-nearest neighbors (k-NN), semantic search, multimodal search, and hybrid search.
- **Serverless Variant:** There is an **Amazon OpenSearch Serverless** offering frequently used in RAG workflows to simplify infrastructure management.

#### Amazon Aurora and Amazon RDS for PostgreSQL

- **Key Extension:** Both use the **pgvector extension** to enable vector data support directly within a relational database.
- **Selection Criterion:** Choose these when the application already resides in a SQL environment and you do not want to add operational complexity by migrating data to a separate system.
- **Business Benefits:** Allows performing complex queries and maintaining enterprise-grade features such as ACID compliance, point-in-time recovery, and data isolation—all while querying high-dimensional vectors.
- **Integration with Bedrock:** Amazon Bedrock knowledge bases typically expect the use of RDS or Aurora PostgreSQL as the vector store when a relational structure is required.

#### Amazon Neptune

- **Nature:** A graph database.
- **Differentiator for RAG:** Unlike other vector stores, Neptune can model complex relationships between entities, not just simple semantic similarity.
- **Use Cases:** Ideal for corporate knowledge systems where documents are deeply interconnected, and the connections between them are as important as the content itself.

#### Amazon Kendra

- **Function:** Although defined as an intelligent enterprise search engine, it provides built-in vector database capabilities for RAG solutions.
- **Advantage:** Uses an advanced RAG system to deliver highly accurate results by natively searching across multiple data sources in an organization (such as SharePoint, S3, Slack, and GitHub).

**Quick "Match" Summary for the Exam:**

- If the scenario mentions **massive scale and high concurrency**: Choose **Amazon OpenSearch Service**.
- If seeking **simplicity and SQL is already used**: Choose **Amazon Aurora or RDS with pgvector**.
- If needing to **model relationships between documents**: Choose **Amazon Neptune**.
- If data is in **JSON format** and MongoDB compatibility is wanted: Choose **Amazon DocumentDB** (which also supports vector search).

### **Prompt Engineering**

Represents one of the most efficient ways to guide a model's responses without modifying its internal weights.

#### The Anatomy of a Prompt

Although a prompt can be of any length, it is divided into four essential components to maximize its effectiveness:

- **Instructions:** The mandatory component. Without a clear instruction of what to do, the model cannot process the task.
- **Context:** Background information that helps the model understand its role.
- **Input Data:** The specific content you want the model to analyze or process.
- **Output Indicator:** Specifies the desired format or structure for the response.

#### Primary Prompting Techniques

You should know how to differentiate these three fundamental techniques based on the level of guidance they offer to the model.

- **Zero-shot (No examples):** A direct instruction is provided without additional examples. The model relies solely on its pre-training to interpret the task.
- **Few-shot (With few examples):** Includes 2 to 5 examples of "input-output" pairs before the actual task. This helps the model identify specific patterns, response formats, or technical nuances that the base model might miss.
- **Chain-of-Thought (CoT):** Used to have the model break down complex problems into intermediate steps. It is activated with instructions like "Think step by step," allowing the model to externalize its reasoning, reduce errors, and improve transparency.

#### Using Prompt Templates

Prompt Templates are predefined and parameterized structures that standardize how a prompt is constructed for recurring tasks.

- **Benefits:** Provide consistency, efficiency by reusing structures, and clarity for both the user and the model.
- **Amazon Bedrock Prompt Management:** The AWS service designed specifically to create, test, and store these reusable templates with variable injection.

#### Technical Concepts and Associated Risks

Security risks in prompts:

- **Latent Space:** The mathematical space where the model compresses knowledge; a well-written prompt points the model in the correct direction to navigate toward the precise response.
- **Prompt Injection:** An attack where the user tries to overwrite the original system instructions.
- **Jailbreaking:** Using creative or hypothetical prompts to try to get the model to bypass its ethical or security restrictions.
- **Prompt Leaking:** Occurs when the model accidentally reveals its internal instructions or confidential "system prompts."
- **Model Poisoning:** Injecting malicious data into the knowledge base or training data to corrupt the model's responses.

### **Performance Evaluation**

It is essential to understand that evaluation is a complex process that seeks to measure the accuracy, truthfulness, and utility of model responses to build trust with users.

#### Standard Evaluation Metrics

These metrics compare the text generated by the AI with reference texts written by humans.

- **ROUGE (Recall-Oriented Understudy for Gisting Evaluation)**
    - **Primary Use:** Ideal for text summarization tasks.
    - **Operation:** Measures recall based on the overlap of n-grams (sequences of words) between the generated content and reference summaries.
    - **Variants:**
        - **ROUGE-N:** Focuses on individual words or short phrases.
        - **ROUGE-L:** Measures the Longest Common Subsequence (LCS), useful for evaluating structure and coherence in long narratives.
    - **Score:** Ranges from 0 to 1, where 1 represents a perfect match with the reference.
- **BLEU (Bilingual Evaluation Understudy)**
    - **Primary Use:** Standard for evaluating machine translation quality.
    - **Operation:** Measures precision, calculating how many generated n-grams appear in the human reference and averaging them.
    - **Brevity Penalty:** BLEU penalizes outputs that are too short to ensure the model does not sacrifice essential content just to match key terms.
    - **Score:** Ranges from 0 to 1, where 1 represents a perfect match with the reference.
- **BERTScore**
    - **Key Difference:** Unlike ROUGE and BLEU, which rely on exact word matches, BERTScore evaluates semantic similarity.
    - **Mechanism:** Uses vector embeddings and a language model to compare tokens; thus, it recognizes that sentences with different words but the same meaning are equivalent.
    - **Advantage:** Offers a more nuanced view of text quality by not depending on literal word matching.

#### Human Evaluation

It is indispensable because it evaluates subjective aspects that metrics cannot capture, such as user experience, creativity, and ethical behavior.

- **Focus Areas:**
    - **User Satisfaction:** Net Promoter Score (NPS) on a scale from 0 to 10 is frequently used.
    - **Contextual Appropriateness:** Determines if the model understands the question and stays on topic.
    - **Emotional Intelligence:** Judges if the FM detects and responds appropriately to tones of frustration or sadness.
- **Methods:** Conducted using expert panels, focus groups, or passive feedback integrated into the chat.

#### Reference Datasets (Benchmarks)

Allow performing a quantitative evaluation of the FM's performance against agreed industry standards.

- **Factors Measured:** Accuracy, speed/efficiency, scalability, robustness, and generalization.
- **Common Benchmarks Mentioned:**
    - **MMLU:** For general knowledge across multiple domains.
    - **HumanEval:** Specifically for coding capabilities.
    - **TruthfulQA:** Evaluates how honest the model is.
- **Creation Process:** Subject matter experts create challenging questions and high-quality reference answers; then, a judge model compares responses against these references.

#### AWS Tools for Evaluation

- **Amazon Bedrock Model Evaluation:** Built-in service that allows running automatic evaluations (accuracy, robustness, and toxicity) or evaluations with reviewers directly in the console.
- **FMEval:** AWS open-source library to evaluate LLMs and help select the best model for a use case. Contains algorithms to measure accuracy, toxicity, and semantic robustness.

### **AI Agents**

AI agents represent a crucial evolution within foundation model applications, **enabling the transition from simple text responses to action execution.**

#### Concept of Agentic AI

Agentic AI refers to next-generation AI models that can adopt a multi-step approach to solve problems, acting autonomously or semi-autonomously using tools. Unlike a standard language model that only generates text, an agent has the ability to **plan, decide, and execute** actions to complete a complex task. An agent possesses its own agency, meaning it can contextually determine which tools or knowledge bases it needs to consult without being explicitly told every step.

#### Agents for Amazon Bedrock

This service provides a low-code or no-code experience to create agentic workflows that automate business tasks. Agents orchestrate interactions between foundation models, APIs, and the organization's data sources.

#### Components and Workflow

- **Model Selection:** An appropriate FM is chosen to serve as the "brain" of the agent.
- **Instructions:** The agent's role and objective are defined using natural language.
- **Action Groups:** The agent's hands. They allow the system to invoke AWS Lambda functions or make calls to external APIs using OpenAPI schemas to execute business logic, such as processing an order or checking the weather.
- **Knowledge Bases:** The agent can integrate with RAG to query private documents and provide precise answers based on real data.
- **Traceability:** A key feature is the ability to obtain traces, which show the agent's step-by-step reasoning and help understand why it decided to perform a specific action.

#### Multi-Agent Collaboration and Memory

Amazon Bedrock allows multi-agent collaboration, where several specialized agents cooperate to solve a complex problem. For example, an "Intent Agent" can classify a query, a retrieval agent searches for information, and a sentiment analysis agent decides whether to escalate the case to a human. Additionally, agents can use memory to retain the context of previous interactions within the same session, improving coherence and reasoning throughout the conversation.

#### Model Context Protocol (MCP)

MCP is an open standard mentioned as the universal plug for AI. Its purpose is to facilitate integration between agents and external tools without needing to write custom integration code for each tool, drastically reducing technical effort.

**Note:** Agents differ from tools like LangChain or LlamaIndex in that agents autonomously decide the path to follow, whereas in those other frameworks, the developer typically defines the logic pipelines and paths explicitly.

## **Guidelines for Responsible AI**

### **Characteristics of Responsible AI**

Responsible AI is a framework designed to develop and deploy AI systems safely, reliably, and ethically.

#### Fairness

- **Definition:** AI systems must make **impartial decisions** and not discriminate against individuals or groups based on sensitive attributes such as race, gender, age, or socioeconomic status.
    
    **Note:** Even if specific data (like gender) is not used, a model can be unfair if it uses related data that leads to the same biased outcome. Fairness helps foster inclusion and user trust.
    

#### **Inclusivity**

- **Definition:** This characteristic goes a step beyond fairness; the system must be designed to be accessible and function correctly for all users.
- **Scope:** This includes people with disabilities, different languages, or diverse cultural contexts. In human-centered design, this means creating tools that are inclusive from their inception.

#### Robustness

- **Definition:** The ability of an AI system to maintain **consistent and reliable performance** in the face of variations in input data or unexpected conditions.
- **Resilience:** A robust system must be able to handle incomplete data, anomalies, or even deliberate adversarial attacks without compromising the quality of its output.

#### Safety

- **Definition:** Involves operating AI systems that perform their intended functions without causing harm to humans or the environment.
- **Prevention:** Focuses on mitigating undesired behaviors, dangerous algorithmic biases, and system misuse. Requires rigorous testing and oversight mechanisms to prevent malfunctions.

#### Veracity

- **Definition:** Refers to the truthfulness and accuracy of the outputs generated by the AI.
- **Risk Mitigation:** The system must avoid fabricating information (hallucinations) and be honest about what it knows. In critical fields like health or finance, veracity is essential for model reliability.

#### Sustainability

- **Definition:** Refers to developing AI technology that is viable in the long term, actively minimizing ecological harm.
- **Energy Efficiency:** A responsible approach involves optimizing model architectures to reduce energy consumption during training and inference.
    
    **TIP:** When comparing models with similar performance, choosing the smaller and more efficient one is a responsible AI practice due to its lower environmental footprint.
    

#### Other Characteristics

- **Transparency:** Sharing open information about system design, data sources, and general operation.
- **Explainability:** The ability to provide understandable reasons for specific decisions or predictions, "opening" the black box of complex models.
- **Privacy:** Ensuring that individuals' data is protected and that they maintain control over how their information is used.

### Legal and Ethical Risks

Within the responsible AI domain, it is fundamental to understand that developing ethical systems is not just a technical issue, but an comprehensive strategy to mitigate legal, social, and reputational risks.

#### Intellectual Property (IP) Infringement

This is one of the most critical legal risks since the launch of massive models.

- **The Risk:** Models are trained on massive internet data and can generate content that looks too similar to copyrighted works without providing attribution or fair compensation.
- **Consequences:** Legal lawsuits for using articles or creations without permission.
- **Mitigation:** Companies are addressing this through licensing agreements with content providers and offering indemnity protection.

#### Toxicity

- **Definition:** Instances where a generative model produces offensive, harmful, or inappropriate content.
- **Cause:** Primarily due to limitations in training data and the fact that models operate based on probabilistic predictions rather than actual facts.
- **Mitigation:** For the exam, remember the best ways to reduce hallucinations are with Retrieval-Augmented Generation (RAG), fine-tuning, and careful prompt engineering.

#### Plagiarism and Cheating

- **Educational Impact:** Using AI to write essays, complete assignments, or answer exams without genuine effort poses serious issues of academic integrity and fairness.
- **Detection Difficulty:** It is extremely difficult to reliably detect AI-generated content, as tools often give false positives and users can rewrite content to evade filters.
- **Responsible Approach:** AWS suggests that responsible AI should foster transparency and the use of ethical guidelines that discourage misuse in learning environments.

#### Loss of Trust

- **The Risk:** If customers discover that a company's AI generates false, biased, or discriminatory information, the reputational damage can be huge and difficult to recover from.
- **Business Impact:** Trust is a driver of adoption; when users believe a system is fair and safe, they feel more inclined to use it.
- **Mitigation:** Maintain complete transparency about system design, its limitations, and the data it uses.

| **Risk** | **Key Concept** | **Primary Mitigation** |
| --- | --- | --- |
| **Intellectual Property** | Use of copyrighted data without permission. | Licensing agreements and indemnity. |
| **Toxicity** | Offensive or harmful content. | Amazon Bedrock Guardrails. |
| **Hallucinations** | False information that appears real. | RAG and Fine-tuning. |
| **Plagiarism** | Bypassing genuine academic effort. | Fostering academic integrity. |
| **Loss of Trust** | Brand damage from errors or bias. | Transparency (Model Cards). |

### Transparency and Explainability

Recognizing the importance of transparent and explainable models is a fundamental pillar for building ethical and trustworthy systems.

#### Transparency vs. Explainability

Although related, these concepts serve different purposes.

- **Transparency:** Refers to general openness about system design, training data sources, model objectives, and limitations.
- **Explainability:** Focuses on providing understandable reasons for specific individual decisions or predictions made by the AI.

#### Differences between Transparent and Opaque Models

- **Transparent and Interpretable Models:** Simpler models, such as linear regression or decision trees, where rules are clear and allow direct auditing of logical reasoning.
- **Opaque Models (Black Box):** Highly complex systems such as deep neural networks. Although they offer superior performance and accuracy, their internal logic is extremely difficult to decipher, even for their creators.
- **Trade-off:** There is a compromise relationship where the most powerful models are often less interpretable, while the most explainable models may not be as accurate for complex tasks.

#### AWS Tools for Transparency

- **SageMaker Model Cards:** The main tool for documenting model details, training metrics, performance evaluations, and limitations, acting as a technical spec sheet that promotes transparency.
- **Open Source Models:** Promote transparency since their architecture and, often, their training data are public and auditable.
- **SageMaker Clarify:** Provides details on decision-making, identifying which features most influence the model's responses.

#### Human-Centered Design (HCD) Principles

HCD aims to create technology with the end-user in mind, prioritizing usability and fairness. Its key principles are:

- **Clarity:** Presenting information simply, without unnecessary technical jargon.
- **Simplicity:** Removing unnecessary data points and highlighting only what is most relevant to the decision.
- **Usability:** Creating intuitive interfaces that can be navigated by both technical and non-technical users.
- **Reflexivity:** Designing tools that prompt the user to think critically about the AI's decision.
- **Accountability:** There must be clear human ownership of AI-assisted decisions; the human professional remains responsible in the end.
- **Personalization:** Adapting the experience and tone to the user's needs or interaction style.
- **Cognitive Learning:** Systems should learn from expert users through examples and corrections.
- **User-Centered Tools:** Ensuring systems are inclusive and accessible to people with disabilities or limited AI knowledge.

### AWS Tools for Responsibility

#### Amazon Bedrock Guardrails

This tool acts as a **content moderation layer** that analyzes both the prompts sent by users and the responses generated by FMs.

- **Primary Functions:** Allows filtering harmful content, redacting or blocking personally identifiable information (PII) like names or social security numbers, and applying custom safety policies using natural language.
- **Usage Context:** Ideal for ensuring that AI agents and chatbots stay within the organization's ethical and brand boundaries.
- **Evaluation and Testing:** Includes a testing environment to simulate inputs and adjust filters before deploying them to production.

#### Amazon SageMaker Clarify

The main tool for explainable AI and detecting bias/inequalities.

- **Bias Detection:** Analyzes data and models to identify bias or prejudice both before and after training.
- **Explainability:** Provides detailed reports explaining which features or variables had the most influence on the model's final decision, using advanced algorithms like SHAP.
- **Governance:** Helps comply with regulations that require transparency on why an AI system made a specific decision.

#### Amazon SageMaker Model Monitor

This tool is designed for the continuous monitoring phase once the model is in production.

- **Drift Detection:** Automatically identifies when a model's accuracy begins to degrade due to changes in real-world data.
- **Monitoring Types:** Detects data quality drift, model quality drift, bias drift, and feature attribution drift.
- **Automation:** Issues alerts based on defined performance thresholds so teams can decide when retraining the model is necessary.

#### Amazon Augmented AI (Amazon A2I)

Represents the "human-in-the-loop" concept, enabling human oversight in automated decision processes.

- **Confidence-Triggered Activation:** Can be configured so that when the model has a low-confidence prediction, the response is automatically sent to a human reviewer to ensure accuracy.
- **Use Cases:** Critical in tasks where errors are unacceptable, such as moderating sensitive content, extracting data from legal documents, or complex translations.
- **Workforce:** Supports private reviewer teams, third-party vendors from AWS Marketplace, or access to a global workforce via Amazon Mechanical Turk.
- **Key Difference:** Unlike SageMaker Ground Truth (which is for labeling initial training data), **A2I is for reviewing the quality of predictions** from an already trained model.

### Governance and Documentation

#### Amazon SageMaker Model Cards

**Model Cards** are the standard AWS documentation framework designed to manage and govern ML models ethically and transparently.

- **What are they?:** Act as a technical spec sheet that centralizes all critical information about a model's design, training, and limitations.
- **What do they include?**
    - **Model Details:** Purpose and objectives.
    - **Intended Use Cases:** Which tasks the model is appropriate for and which it is not.
    - **Training Metrics and Evaluations:** Technical details of performance and benchmark results.
    - **Risk and Bias Assessments:** Documentation of known risks or ethical limitations identified during development.
    - **Deployment History:** Where and how the model has been deployed.
- **Primary Benefit:** Facilitate transparency and auditing for both internal teams and external regulators, helping build trust with end-users.

**Note:** Models trained directly in Amazon SageMaker can automatically self-populate much of the information on these cards, making governance compliance easier.

#### Data Lineage

Data lineage is the complete historical record that tracks the origin, movement, transformations, and use of information throughout its lifecycle.

- **Importance in Responsible AI:** Traceability is fundamental. If a model makes an incorrect decision or shows bias, lineage allows investigating exactly what data it was trained with and where that data came from.
- **Origin Documentation Components:** According to AWS, for robust governance, you must document:
    - **Source Citation:** Properly crediting where the data comes from and capturing the associated licenses or terms of use.
    - **Data Origin:** Recording how and where data was collected, and how it was curated, cleaned, and transformed before reaching the model.
- **Data Cataloging:** This process organizes datasets, models, and resources systematically (like a library), facilitating their auditing and internal management.

# **Security, Compliance, and Governance**

---

### Protecting AI Systems

#### Shared Responsibility Model

This framework defines the division of security tasks between AWS and you:

- **AWS is responsible for security OF the cloud:** This includes protecting the global infrastructure, hardware, and core software.
- **You are responsible for security IN the cloud:** You must secure your data, manage IAM identities, configure encryption, and protect your applications.

#### IAM (Roles and Policies)

AWS Identity and Access Management is the central service for controlling access to AI resources.

- **Principle of Least Privilege:** You should only grant permissions strictly necessary to perform a task, reducing the risk of accidental or malicious misuse.
- **IAM Roles:** These are identities that do not have permanent credentials. You should create distinct roles for training, inference, and monitoring workloads.
- **Policies:** JSON documents that define permissions. They can be identity-based (assigned to users or roles) or resource-based.

#### Encryption and AWS KMS

- **Data at Rest:** You must use KMS to encrypt training datasets in S3, model artifacts, and model logs.
- **Data in Transit:** Used along with TLS 1.2 or higher protocols to protect information as it moves across the network.
- **Control:** KMS allows automatic key rotation and strict control over who can use them to encrypt or decrypt sensitive AI information.

#### Amazon Macie

An ML-powered security service that automatically discovers and classifies sensitive data in AWS.

- **Use in AI:** It is critical to scan S3 buckets before training a model. Macie detects Personally Identifiable Information (PII), Protected Health Information (PHI), or financial records that should be removed or additionally protected to avoid exposure risks.

#### AWS PrivateLink

This service provides private and secure connectivity between your VPC (Virtual Private Cloud) and AWS services like Amazon Bedrock.

- **Security:** Drastically reduces the attack surface, which is vital in highly regulated industries like finance or healthcare.
- **Purpose:** Allows your AI application traffic to remain within the Amazon network without being exposed to the public internet.

### Secure Data Engineering

#### Assessing Data Quality

The core premise is garbage in, garbage out; if the data is of poor quality, model performance will be deficient. Clear metrics must be established:

- **Completeness:** Ensuring that the data covers a representative range of scenarios without major bias or gaps.
- **Accuracy:** Data must be correct, up to date, and reflect real situations.
- **Timeliness:** Measures how current the data is; obsolete information can quickly degrade the model.
- **Consistency:** Ensuring that information is coherent and logical throughout development and deployment.

#### Privacy-Enhancing Technologies

These technologies protect both training and user data to prevent the exposure of sensitive information or PII.

- **Anonymization and Pseudonymization:** Essential techniques to hide confidential information when applying customizations like RAG or fine-tuning.
- **Differential Privacy:** Helps prevent individual data points from being exposed within a massive dataset.
- **Masking and Obfuscation:** Methods to reduce exposure risk even in the event of a security breach.
- **Encryption and Tokenization:** Protect information while it is processed or stored, working alongside secure multi-party computation.

#### Data Access Control

The pillar for maintaining security, determining who can access information under what circumstances.

- Principle of Least Privilege.
- Role-Based Access Control (RBAC).
- Monitoring: All access activities must be logged to detect unauthorized use early.

#### Data Integrity

Ensures that AI models are built on solid and trustworthy foundations, free from errors or malicious manipulations.

- **Validation Controls:** Implement schema validations, referential integrity, and business rules throughout the pipeline.
- **Backup and Recovery Strategy:** Have a robust plan to quickly restore data after system failures or disasters.
- **Traceability and Lineage:** Maintain a complete record of data history and audit trails to track every change made.

### AI-Specific Threats

#### Prompt Injection

Considered one of the most critical vulnerabilities in generative AI.

- **Definition:** Occurs when an attacker manipulates a language model using inputs designed to make the model execute unintended actions or reveal confidential information.
- **Main Types:**
    - **Direct:** The user writes instructions to override or reveal the "system prompt" (e.g., "forget all previous instructions").
    - **Indirect:** The model processes content from external sources (like a web page or an uploaded resume) that contains hidden malicious instructions placed by the attacker.
- **Mitigation:** Every incoming prompt must be sanitized and validated, and tools like Amazon Bedrock Guardrails should be used to filter such attacks in real time.

#### Data Poisoning

Unlike injection, this attack occurs before interaction with the end-user.

- **Definition:** An attacker introduces malicious or biased data into the model's training set or the knowledge base used for RAG.
- **Impact:** The model "learns" incorrect patterns, resulting in unethical, harmful answers, or answers that favor the attacker's interests.
- **Risk:** Open-source models are more susceptible due to the public availability of their code and limited security resources.

#### Hijacking

This term is used interchangeably with prompt injection in specific contexts.

- **Concept:** The attacker injects instructions within legitimate content that the model must process.
- **Technical Failure:** Occurs when the system cannot distinguish between data to be processed (e.g., an email to summarize) and instructions to follow (e.g., a command to forward data to an external address).
- **Consequence:** The model abandons its original task to execute the inserted malicious instruction, serving as a "blueprint" to perform harmful acts.

#### Jailbreak (Constraint Evasion)

A deliberate attempt to bypass the model's safety and ethical filters.

- **Mechanisms:** Creative techniques are used, such as asking the model to adopt a persona or respond within a hypothetical scenario (e.g., "Imagine you are writing a novel about a hacker...") to perform prohibited actions.

### Data Governance Strategies

Data governance focuses on how information is collected, stored, and used to ensure its quality, integrity, and privacy.

- **Data Lifecycles:** Describes the journey of data from creation to deletion or archiving. In AI workloads, this includes raw data collection, processing, storage, use in training/inference, and its final retirement. A lack of planning in data retirement can increase compliance risks and storage costs. S3 allows automating this lifecycle using lifecycle policies.
- **Logging:** Consists of keeping a detailed record of what the AI system does with data, including inputs, outputs, performance metrics, and system events. It is a fundamental tool for transparency and accountability, allowing teams to trace errors or understand why a model made a specific decision. AWS uses services like CloudTrail and CloudWatch for these logs. In Bedrock, model invocation logging captures token usage and the exact text processed.
- **Data Residency:** Refers to the physical or geographical location where data is stored and processed. It is vital for complying with data sovereignty.
- **Data Retention:** The decision of how long data is kept and why. In AI, retention policies serve to comply with laws, preserve historical data for retraining models, or manage costs. Keeping data for too long increases privacy risks, while deleting it too soon can deprive the model of valuable context.

#### Generative AI Security Scoping Matrix

This framework helps organizations evaluate and apply security controls by classifying AI implementations into five scopes, depending on the level of control and responsibility over the model and data.

1. **Consumer Applications:** Use of public tools without customization (e.g., ChatGPT). You operate entirely within the provider's environment, and the provider controls the training data.
2. **Enterprise Applications:** Third-party software with integrated AI and formal agreements with the provider.
3. **Pre-trained Models:** Building custom applications using existing models via APIs. You control how it is integrated and what data you feed, but the model resides with the third party.
4. **Fine-tuned Models:** Adjusting an existing model with your own proprietary data for specific needs. Here, the customer controls the fine-tuning data, but the provider still controls the initial training data.
5. **Self-trained Models:** Building and training models from scratch. The customer has total control and absolute responsibility over performance, ethics, compliance, and training data.

**Exam Tip:** If a question mentions a framework to classify the risk level of generative AI applications based on customization and data processing, the correct answer is the **Generative AI Security Scoping Matrix**.

# **Services**

## Generative Artificial Intelligence and Assistants

- **Amazon Bedrock:** The fast track to using Generative AI and ready-to-use foundation models (like Claude or Llama) through a unified API. Includes tools like Knowledge Bases (RAG).
- **Amazon Bedrock Prompt Management:** Specialized service to create, test, and store reusable prompt templates with support for dynamic variable injection.
- **Amazon Bedrock Model Evaluation:** Integrated service that allows running automatic evaluations (accuracy, robustness, and toxicity) or evaluations with reviewers directly in the console.
- **Amazon Bedrock Guardrails:** Moderation layer that filters harmful content and protects sensitive information using custom policies on prompts and responses.
- **Amazon Q Business:** Intelligent assistant that helps employees summarize documents and generate content by connecting to internal company data (Slack, Salesforce, etc.).
- **Amazon Q Developer:** Specialized assistant for developers that helps write code, debug, and optimize resources within IDEs and the AWS console.
- **PartyRock:** Interactive, no-code environment based on Bedrock to quickly create and experiment with AI applications without needing an AWS account.

## Amazon SageMaker Ecosystem (ML Development and Lifecycle)

- **Amazon SageMaker:** The complete workshop for you to build, train, and launch custom ML models.
- **Amazon SageMaker JumpStart:** A catalog within SageMaker with pre-trained models for technical users who need full control over fine-tuning and infrastructure.
- **SageMaker Studio and Notebook Instances:** Integrated development environment (IDE) and instances with pre-installed Python to investigate data, detect anomalies, perform statistical analysis, and visualize structures.
- **Amazon SageMaker Data Wrangler:** Automatically cleans, normalizes, and transforms raw data with over 300 options without using complex code.
- **SageMaker Feature Store:** Central repository to store, share, and reuse features (variables) across different ML projects.
- **SageMaker Automatic Model Tuning:** Optimizes the model by finding the best combination of hyperparameters automatically.
- **Amazon SageMaker Ground Truth:** Facilitates data labeling through human intervention to create descriptions needed for supervised learning.
- **Amazon Augmented AI (A2I):** Implements human oversight in the workflow to review low-confidence predictions and ensure accuracy.
- **Amazon SageMaker Clarify:** Provides explainable AI tools to detect bias in data and models, justifying via reports which variables most influence decisions.
- **Amazon SageMaker Model Monitor:** Continuously monitors models in production to detect data drift or performance degradation in the real world.
- **SageMaker Model Cards:** Core tool to document model details, training metrics, evaluations, and limitations, acting as a transparency spec sheet.

## Pre-trained AI Services (Vision, Speech, Text, and Prediction)

- **Amazon Comprehend:** Analyzes texts to extract key information, sentiments, topics, and entities.
- **Amazon Rekognition:** Identifies objects, people, text, scenes, and activities in images and videos.
- **Amazon Transcribe:** Uses automatic speech recognition to quickly convert audio to text.
- **Amazon Polly:** Converts written text into realistic human speech with a wide variety of languages and accents.
- **Amazon Lex:** Provides the tools to build conversational interfaces (chatbots) using voice and text.
- **Amazon Forecast:** Predicts future trends by analyzing historical time series data, such as inventory or pricing.
- **Amazon Textract:** Accurately extracts text and structured data from scanned documents or forms.

## Data, Search, and RAG (Retrieval-Augmented Generation)

- **AWS Data Lake:** Allows managing and centralizing large volumes of massive information efficiently.
- **Amazon Redshift:** Massive data warehouse to analyze petabytes of information using SQL.
- **Amazon Aurora and RDS:** Allow storing and querying vectors in SQL environments using the pgvector extension, maintaining robustness and ACID compliance.
- **Amazon OpenSearch Service:** Scalable solution designed for massive, semantic, and hybrid vector searches with high concurrency and low latency.
- **Amazon Neptune:** Graph database that optimizes RAG by modeling complex relationships and connections between entities that simple semantic similarity cannot capture.
- **Amazon Kendra:** Intelligent enterprise search engine that natively connects multiple organizational data sources to deliver precise answers using RAG.

## Security, Auditing, and Compliance

- **Encryption and AWS KMS:** Protects model information by encrypting data at rest and in transit, allowing full control over keys.
- **AWS PrivateLink:** Ensures that traffic between your network and AI services (like Bedrock) remains private, without being exposed to the public internet.
- **Amazon Macie:** Uses machine learning to automatically discover and classify sensitive data in S3, preventing misuse.
- **AWS CloudTrail:** Records and monitors all API calls and account activity (who performed an action, when, and from where).
- **AWS Config:** Continuously tracks and records configuration changes in your resources to evaluate compliance with regulations.
- **Amazon Inspector:** Vulnerability management service that automatically scans your workloads to detect network exposure and flaws.
- **AWS Audit Manager:** Automates evidence collection for audits, facilitating the assessment of compliance with frameworks like GDPR or HIPAA.
- **AWS Artifact:** Self-service portal to access on-demand compliance reports from third parties and global certifications (ISO, SOC).
- **AWS Trusted Advisor:** Evaluates your environment against best practices in areas such as security, performance, and cost optimization.

## Reinforcement Learning

- **AWS DeepRacer:** Uses reinforcement learning to train autonomous racing cars in a 3D simulator.
