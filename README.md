# Conversational-Medical-Assistant-Using-Rasa
This repository contains the implementation of a Conversational Medical Assistant, designed to provide preliminary medical assistance using a chatbot framework. Built with the Rasa Open Source Framework and integrated with a Neo4j knowledge graph, this project demonstrates the practical application of natural language understanding (NLU), dialogue management, and structured data in delivering impactful healthcare solutions


# Features
Natural Language Understanding (NLU):

Configured pipelines for intent classification, entity extraction, and synonym mapping using Rasa’s powerful NLU components. Handles user intents such as symptom inquiry, disease prediction, medication suggestions, and appointment scheduling. Implemented custom stories and rules for seamless conversation flow. Supported fallback mechanisms for unrecognized intents and ambiguous user inputs.



Neo4j Knowledge Graph Integration:

The chatbot retrieves structured medical information using a Neo4j database, enhancing its contextual understanding and providing accurate responses. The knowledge graph connects entities like symptoms, diseases, medications, and treatments to ensure comprehensive data retrieval.



Custom Actions:

Implemented server-side actions to query Neo4j and dynamically generate responses tailored to user queries. Leveraged Python scripts to establish connectivity with the Neo4j database via the Neo4j Python driver. Designed to support integration with various front-end interfaces such as web applications, mobile apps, or voice assistants. Configured Rasa's endpoints for real-time interactions and API integrations.


#Overview
1. Rasa Framework

NLU Pipeline:
Utilizes tokenization, intent classification (e.g., DIETClassifier), and entity recognition to process user inputs efficiently.
Stories and Rules:
Dialogue flow is defined through curated stories for multi-turn conversations and rules for deterministic responses.
Domain Configuration:
Includes intents, entities, slots, responses, actions, and forms for managing the chatbot’s behavior.



2. Neo4j Knowledge Graph
The Neo4j database serves as the backend for storing and retrieving medical data. The schema models relationships between medical entities, such as:

Symptoms → Associated Diseases
Diseases → Possible Medications
Diseases → Recommended Specialists
Queries are executed using Cypher, Neo4j's declarative query language, to fetch relevant data dynamically.



3. Custom Action Server
The action server interacts with Neo4j using the Neo4j Python driver. Key functionalities include:
Querying the knowledge graph for disease prediction based on symptoms provided by the user.
Recommending medications and next steps for medical assistance.
Providing a fallback response for edge cases where no information is available.



4. System Workflow
User Input: The user queries the chatbot using natural language (e.g., “I have a fever and headache”).
Intent and Entity Recognition: The input is processed to extract intents (symptom_inquiry) and entities (fever, headache).
Dialogue Management: Based on the conversation history, the chatbot determines the next action (e.g., querying the knowledge graph).
Neo4j Query Execution: The action server fetches data related to the symptoms from Neo4j and formulates a response.
Response Generation: The chatbot delivers the output to the user in a conversational format.


#Installation and Setup
Clone the Repository

bash
Copy code
git clone   
Install Dependencies
Install the required Python packages:

bash
Copy code
pip install -r requirements.txt  
Set Up Neo4j

Install Neo4j Community Edition.
Import the provided knowledge_graph.cypher file to populate the database.
Configure Rasa

Train the NLU and Core models:
bash
Copy code
rasa train  
Run the Rasa server:
bash
Copy code
rasa run --enable-api  
Start the Action Server

bash
Copy code
rasa run actions  
Testing the Bot
Interact with the bot locally using:

bash
Copy code
rasa shell  
