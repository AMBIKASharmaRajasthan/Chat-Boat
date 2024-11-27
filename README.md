# GPT Chatbot using OpenAI's GPT-3.5 Turbo API

This repository demonstrates the implementation of a chatbot powered by OpenAI's GPT-3.5 Turbo API. It includes tools for crafting effective prompts, utilizing advanced API functionalities, and exploring structured outputs for various applications.

## Features

- Integration with OpenAI's GPT-3.5 Turbo API.
- A reusable helper function for generating responses.
- Demonstrations of advanced prompting techniques:
  - Few-shot prompting
  - Instruction-based prompting
  - Structured outputs in formats like JSON and HTML.
- Clear guidelines for customizing temperature and response styles.

## Prerequisites

Before running this project, ensure you have:

1. **Python**: Version 3.7 or higher.
2. **OpenAI API Key**: API key from [OpenAI's API dashboard](https://platform.openai.com/account/api-keys).
3. **Dependencies**: Install required Python libraries using the provided `requirements.txt`.

## Installation

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Set Up Your OpenAI API Key
Create a `.env` file in the project root and add your API key:
```
OPENAI_API_KEY=your_openai_api_key
```

Alternatively, set the environment variable directly:
```bash
export OPENAI_API_KEY='your_openai_api_key'
```

## Usage

### 1. Helper Function for Chat Completion
The script provides a `get_completion` function to simplify interactions with the GPT-3.5 Turbo API:
```python
from helper import get_completion

prompt = "What is the capital of France?"
response = get_completion(prompt)
print(response)  # Output: "The capital of France is Paris."
```

### 2. Examples of Prompting Techniques
Explore different techniques for interacting with GPT:

#### Structured Output in JSON
```python
prompt = """
Generate a list of three made-up book titles along with their authors and genres.
Provide the output in JSON format.
"""
response = get_completion(prompt)
print(response)
```

#### Few-shot Prompting
```python
prompt = """
<child>: Teach me about patience.

<grandparent>: The river that carves the deepest valley flows from a modest spring.

<child>: Teach me about resilience.
"""
response = get_completion(prompt)
print(response)
```

### 3. Running the Example Script
Use `main.py` to test the chatbot:
```bash
python main.py
```


## Customization

### Modify Temperature
Adjust the randomness of the responses by modifying the `temperature` parameter in `helper.py`:
```python
temperature=0.7
```

### Change Model
Switch between GPT models (e.g., `gpt-3.5-turbo`, `gpt-4`) by updating the `model` parameter:
```python
model="gpt-4"
```
