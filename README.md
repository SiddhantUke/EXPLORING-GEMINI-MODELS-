Step 1 ) Overview of Gemini Models


Step 2 ) Go to Google aistudio.google.com 
For creating API KEY .
Then Use it and store it in environment variables.

So CLICK ON GET API KEY 
Create an API KEY

We have some free Limit as well
15 Requests Per Minutes 
1 million Tokens per Minutes
1500 RPD Request Per Day

If You Never Created Google Cloud Project 
Here 
Go to Google Cloud 
Then Create an Account and Click on Console 
And Create a Project Name and Other stuffs that are Required.

Then 
Back to Creating API KEY
You will find that same project name that you had entered in that console cloud.


Create API Key in Existing Projects 

API Key Generated Successfully.

Step 3 )   Open Google Colab

Click on Secret Key Icon On the left hand side.

If You can't see anything give the access then you will automatically see that API KEY that we had created in the Step 2 


This quickstart demonstrates how to use the Python SDK for the Gemini API, which gives you access to Google's Geminilarge language models. In this quickstart, you will learn how to:

1. Set up your development environment and API access to use Gemini.
2. Generate text responses from text inputs.
3. Generate text responses from multimodal inputs (text and images).
4. Use Gemini for multi-turn conversations (chat).
5. Use embeddings for large language models.

Install THE PYTHON SDK

The Python SDK for the Gemini API, is contained in the google-generativeai package. Install the dependency using pip:

Importing Packages


Responsible for calling various Gemini Models.


To Replace Markdown chatgpt kro ! 



In Order to Call API key We need to set API KEY.

In Order to call that key 
Use this .




SETUP API KEY.

Once you have the API key, pass it to the SDK. You can do this in two ways:

 Put the key in the GOOGLE_API_KEY environment variable (the SDK will automatically pick it up from there).• 

Pass the key to genai.configure(api_key=...) 

#Or use os.getenv('GOOGLE_API_KEY') to fetch an environment variable.



Calling the Models------> 


List modelsNow you're ready to call the Gemini API. 

Use list_models to see the available Gemini models:

gemini-pro: optimized for text-only prompts.
gemini-pro-vision: optimized for text-and-images prompts.

Exploring The Models Here ! 





For text-only prompts, use the gemini-pro model



The generate_content method can handle a wide variety of use cases, including multi-turn chat and multimodal input, depending on what the underlying model supports. The available models only support text and images as input, and text a output.

<>

In the simplest case, you can pass a prompt string to the GenerativeModel.generate content method


Part by Part All Response is visible now ! 



Generate text from image and text inputs

Gemini provides a multimodal model (gemini-pro-vision) that accepts both text and images and inputs. The GenerativeModel.generate_content API is designed to handle multimodal prompts and returns a text output.


Let's include an image:
