# Self-corrective Coding-Assistant using flow-engineering and langgraph's worklows 
## Self-Correcting Coding Assistant

This project implements a coding assistant with the following features:

* **Code Generation:** Generates code solutions using [Mistral AI](https://mistral.ai/) and [Gemini](https://developers.generativeai.google/).
* **Routing:** Routes user queries to the appropriate LLM based on the topic using [Cohere](https://cohere.ai/).
* **Error Correction:** Checks generated code for errors and iteratively refines it using [LangChain](https://python.langchain.com/).
* **Graph-Based Workflow:** Uses a state graph defined with [LangGraph](https://github.com/langchain-ai/langgraph) to manage the workflow.

**How it Works:**

1. The user provides a coding question.
2. The Cohere router determines whether to use Mistral AI or Gemini for code generation.
3. The selected LLM generates a code solution.
4. The code is checked for errors.
5. If errors are found, the system either reflects on the error using Gemini or tries generating again based on the flag setting.
6. This process is repeated until a correct solution is found or the maximum iterations are reached.

**Dependencies:**

* `langchain`
* `langgraph`
* `langchain_cohere`
* `langchain_mistralai`
* `langchain_google_genai`
* `bs4`
* `google-colab`
* `IPython`

**Usage:**

1. Install the required dependencies.
2. Set up API keys for the LLMs.
3. Run the code in a Google Colab environment.
4. Ask a coding question.
 
