# Machinix - AI Powered Industrial Machinery Support System
This Github Repo contains flow diagrams of project, and notebooks as well
                                                                                                             
# Project Demo - Youtube
https://youtu.be/9gG7UjHwGqw?si=PqiL78-77XP3Vlr- 

# Technologies used
The entire project is mainly based on Python Programming language
1. We have used **langchain.document_loaders** and **langchain.text_splitter** for converting PDFs into text and then text into chunks. 
2. After converting into chunks, we have used the sentence_transformers library to utilize an open-source Hugging Face model, "**all-mpnet-base-v2**" for converting this text into embedding vectors.
3. We then used **Pinecone Vector Database** to store these embeddings.
4. Using Pinecone's API, we have created a function that retrieves the vectors most similar to the user query, using the metrics of **Cosine Similarity** for similarity search.
5. Pinecone provides the fastest retrieval functionality, making our data retrieval superfast.
6. After retrieval of data, the embedding vectors are converted back to text, and then the text is passed to the **Groq API**.
7. Groq API provides the fastest generation functionality.
8. Groq API uses LPU in the backend, which generates the data superfast.
9. For this data generation, it uses the "**llama3-70b-8192**" model, which generates a user-friendly response so that the user can understand the solution to the problem they are facing.
10. The output is displayed on the interface made using **Flask**.

# Problem this project is solving
In industrial factories or institutions, workers or students face the problem of not being able to handle industrial equipment or, if they face any errors or doubts while handling the tools. In such cases, they have to go to other online platforms to see how to handle the equipment/tools or read the manual to solve the problem they are facing. But this is very time-consuming. Also, if the worker is not equipped with experience with the relevant tools/equipment, he/she will find it hard to understand the working of the tool. This is the problem we are solving through our project.

# How are we adressing the problem
Our project aims to solve this real-world problem by implementing a system in which the user will be able to chat with the system using an interface, and the system will provide accurate solutions to the problems the user is facing while handling the tool/equipment. In this project, we have implemented a RAG (Retrieval-Augmented Generation) architecture, which is a perfect solution for this kind of problem statement. Our system will take input from a user manual/user guide of the tool/equipment. Then, the user who is facing problems while using the tool/equipment will be able to chat with the document. For this, we have implemented a Retrieval-Augmented Generation System. Generally, if the same user asks any AI model on the internet, the AI model will give a generalized solution, which may not be applicable to the specific tool/equipment. The best information about the equipment will be in its own user manual. So, using the user manual to retrieve relevant data according to the user query and using a generative model to generate a proper response for the user to understand is crucial. The user can also ask the system for clarification if they are unable to understand the solution. The key aspect of our project is its speed of providing output compared to traditional RAG models and its information accuracy compared to other generalized models on the internet.

