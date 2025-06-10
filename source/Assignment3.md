
# Assignment 3: Deployment and Integration of Large Language Models (LLMs)

## I. Online Model API: OpenAI

-   An OpenAI account was created and an API key was generated.
    
-   Initial tests were performed using Python with the `openai` library.
    
-   The following capabilities were demonstrated:
    
    -   Prompt-based text generation using `gpt-3.5-turbo`.
        
    -   Customization of outputs using parameters like `max_tokens`.
        
-   Due to usage limits, the API key reached its quota and further access was restricted.
    

## II. Local Model Deployment: Ollama + LLaMA 3

-   Ollama was successfully installed on a Windows-based OMEN 16 machine.
    
-   The `llama3` model was pulled and initialized via the command:
    
    ```bash
    ollama run llama3
    
    ```
    
-   The model downloaded (~4.7 GB) and was verified and executed.
    
-   Basic prompts were tested directly from PowerShell.
    

## III. Development Environment Integration

-   VS Code was used as the primary development environment.
    
-   A Python script was created to interact with the local Ollama model via HTTP requests:
    
    ```python
    import requests
    
    prompt = "Explain the life."
    
    response = requests.post(
        'http://localhost:11434/api/generate',
        json={
            "model": "llama3",
            "prompt": prompt,
            "stream": False
        }
    )
    
    print(response.json()["response"])
    
    ```
    
-   This setup allows for easy integration of LLMs in personal projects and academic tools without requiring online access or API usage limits.
    

## IV. Optional: Research Workflow Optimization (Future Work)

-   Future improvements include integrating the local model into research pipelines for text summarization, data analysis, and technical writing assistance.
    
-   Additional exploration into chaining multiple prompts and context-based workflows is suggested.
    

----------

**Status: Complete** ✅

> Written with [StackEdit](https://stackedit.io/).
