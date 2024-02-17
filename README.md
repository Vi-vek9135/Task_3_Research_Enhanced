# Task_3_Research_Enhanced



# Research Book Name Generator and Enhanced Fact Generation 

This is a Python script designed to generate research book names and enhanced fact generation based on user queries. It utilizes the Google Generative AI API to generate relevant titles.

## Setup

1. **Installation**: Ensure you have the required Python packages installed. You can install them using pip:

    ```
    !pip install -q -U google-generativeai
    ```

2. **API Key**: You need to have a valid API key from Google Generative AI. Store this key securely, either by setting it as an environment variable or using Google Colab's userdata feature.

    ```python
    # Used to securely store your API key
    from google.colab import userdata

    # Fetch and store the API key
    GOOGLE_API_KEY=userdata.get('GOOGLE_API_KEY')
    ```

3. **Model Configuration**: Configure the Generative AI API with your API key.

    ```python
    genai.configure(api_key=GOOGLE_API_KEY)
    ```

## Usage

- **Query**: Define your research topic query.

    ```python
    query = "Murder"
    ```

- **Generating Research Book Names**: The script utilizes a pre-trained generative model to generate research book names based on the provided query.

    ```python
    prompt = to_get_response(query)
    print(prompt)
    ```

- **Fact**: Define your fact query.

    ```python
    fact = "Loan pending with the bank"
    ```

- **Generating Enhanced Fact**: The script utilizes a pre-trained generative model to generate enhanced fact based on the provided fact
    ```python
    prompt = to_get_response(fact)
    print(prompt)
    ```
    

## Code Overview

- `to_get_response(query)`: This function takes a query as input and utilizes a pre-defined generative model to generate a research book name based on the query. It returns a formatted string containing both the query and the generated research book name.

- `model = genai.GenerativeModel('gemini-pro')`: Initialization of the generative model (`gemini-pro` in this case) provided by Google Generative AI.

## Example

- For the query "Murder", the generated research book name might be "Murder Mysteries: Investigative Insights and Legal Analysis".


