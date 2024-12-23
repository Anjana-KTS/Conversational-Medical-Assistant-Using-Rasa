# Conversational-Medical-Assistant-Using-Rasa
This repository contains the implementation of a Conversational Medical Assistant, designed to provide preliminary medical assistance using a chatbot framework. Built with the Rasa Open Source Framework and integrated with a Neo4j knowledge graph, this project demonstrates the practical application of natural language understanding (NLU), dialogue management, and structured data in delivering impactful healthcare solutions


# Features
Natural Language Understanding (NLU):

Configured pipelines for intent classification, entity extraction, and synonym mapping using Rasa’s powerful NLU components. Handles user intents such as symptom inquiry, disease prediction, medication suggestions, and appointment scheduling.


Dialogue Management:

Implemented custom stories and rules for seamless conversation flow. Supported fallback mechanisms for unrecognized intents and ambiguous user inputs. 


Neo4j Knowledge Graph Integration:

The chatbot retrieves structured medical information using a Neo4j database, enhancing its contextual understanding and providing accurate responses. The knowledge graph connects entities like symptoms, diseases, medications, and treatments to ensure comprehensive data retrieval.


Custom Actions:

Implemented server-side actions to query Neo4j and dynamically generate responses tailored to user queries.
Leveraged Python scripts to establish connectivity with the Neo4j database via the Neo4j Python driver.


Scalable Architecture:

Designed to support integration with various front-end interfaces such as web applications, mobile apps, or voice assistants.
Configured Rasa's endpoints for real-time interactions and API integrations.
