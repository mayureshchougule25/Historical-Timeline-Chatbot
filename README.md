# Historical-Timeline-Chatbot

# Overview

Historical Timeline Chatbots is intended to provide users with detailed answers to historical events. Integrate an AI operational query system that uses data records with important historical data and invokes the Vault IoT-API with additional information as needed.

# Features

1.Historical Data Retrieval: Searches a preprocessed dataset for historical events based on user queries.

2.Data Cleaning: Removes inconsistencies in names and refines unknown entries.

3.AI-Powered Responses: Uses the Bolt IoT API to generate responses for queries not found in the dataset.

4.Interactive Chat Interface: Allows users to interact with the chatbot in a conversational manner.

# Install Bolt IoT Library
Execute the following command:
```bash
pip install boltiotai
```
Add the following line in your code:
```python
from boltiotai import openai
```
# Dataset Preprocessing

The chatbot drops unnecessary columns (e.g., Sl. No).

It cleans the Important Person/Group Responsible column by standardizing names and replacing unknown values with Unknown (No specific individual).

# How It Works

1.User Query Processing: Extracts keywords by removing stop words and punctuation.

2.Historical Data Search: Finds the most relevant historical event from the dataset.

3.Fallback to AI: If no matching event is found, the chatbot queries the Bolt IoT API for relevant information.

4.Response Generation: Displays historical details such as the incident name, date, country, place, impact, and important persons/groups involved.

# Limitations

The chatbot relies on dataset accuracy; incomplete or incorrect data may affect responses.

Web search functionality depends on API limitations and available data sources.

# Future Improvements

Enhance dataset quality with more historical events.

Improve NLP processing for better query understanding.

Add support for multiple data sources to enhance search results.

