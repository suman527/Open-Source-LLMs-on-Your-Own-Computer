# suman527-Open-Source-LLMs-on-Your-Own-Computer
Chatbot with Llama 
 
Get the Llama Models  

Download the LLaMA Model: First, you'll need to download the LLaMA models. In the example provided, the Phi-3 mini model is downloaded from Hugging Face. Here's the direct download link for the model you need: 

Model Link: Phi-3-mini-4k-instruct-q4.gguf 

 Hugging Face page for model access:  

Directory After Downloading: After downloading the model, you can use the ls -al command to list the downloaded files on your local system. This will show all necessary files for setting up the model. 

A screenshot of the downloaded local files using ls -al . 

 https://imagekit.io/tools/asset-public-link?detail=%7B%22name%22%3A%221st.png%22%2C%22type%22%3A%22image%2Fpng%22%2C%22signedurl_expire%22%3A%222028-04-28T06%3A35%3A17.834Z%22%2C%22signedUrl%22%3A%22https%3A%2F%2Fmedia-hosting.imagekit.io%2F8c53c32e4e114a76%2F1st.png%3FExpires%3D1840516518%26Key-Pair-Id%3DK2ZIVPTIP2VGHC%26Signature%3DE0wCV6D-aeeKIZOJzw64BDyipHIK5bwYND1mSPtMrOOIV40kj8tCZSEGBFGUaEw4DFT68zmjAuBpQSC3~i5epRj8VKsIWRhpsUa4PSsQB8efP7C804BkX1TN3thy5GbLGkeOnYoHdgZLhY-0yNBWM-axjnrU-bDPt6VYJHD0ESgI6PI~sseQlAUPV1hMbsgYgoWs6CNJRw2-4tfQY1WNq-aRVjBuaguhpHf6fofcoqjcWNU~42d4KHrbZ2eTdE9LjXTEbJ415qzypQpsZwYvvVectvIHmm59b76xFZ7EuU9cMy9mdt-zPpif7x96v8KUR1MgYmlC5LrAvz~5g2ZuZw__%22%7D

Ask a different question in the conversation and A screenshot of the output of the answer.. 

  

 

Use the Chat Template to Carry a Conversation 

Ask the next question in the conversation. Write it down as a complete command. A screenshot of the output in response to the next question in the conversation. 

wasmedge --dir .:.  

--nn-preload default:GGML:AUTO:Phi-3-mini-4k-instruct-q4.gguf  

llama-chat.wasm  

--prompt-template llama-3-chat  

--system-prompt "You are a high school social teacher. Explain the concepts of earth geography." 

  

 

 

Create a Chatbot 

Change the “system prompt” for the chatbot-ui to “You are a tour guide for Western tourists in Japan.” Then, submit the screenshot. Ask a few questions about Japan in chatbot-ui. Submit the screenshots. Configure LobeChat to use the http://localhost:8080/v1 as an "OpenAI API proxy address". Submit the screenshot. Chat on LobeChat. Submit the screenshot. 

 

Project – 2  

Add Knowledge to the Chatbot 

Create a Vector Database for External Knowledge 

The output of curl 'http://localhost:6333/collections/chemistry' and a zip file containing the snapshot from the chemistry collection. 

Screenshot from 2024-11-28 12-24-57Improve the Vector Collection for Longer Context Windows 

The chemistry.csv file you generated. The output of curl 'http://localhost:6333/collections/chemistry'. A zip file containing the snapshot from the chemistry collection. 

Screenshot from 2024-11-28 12-24-57Start an RAG API Server 

Use the API to ask a chemistry question and get an answer and API server log that shows the user question, vector search results, and the updated prompt 

Create a Web-based Chatbot 

The publicly accessible chatbot URL and a screenshot of the chatbot UI showing a relevant conversation 

Screenshot from 2024-11-28 16-11-25 

Create a Discord Bot 

An invite link to the Discord server that is hosting the bot and a screenshot of the Discord bot showing a relevant conversation 

 

Project - 3 

Fine-Tune the Llama Model 

Create the Training Dataset 

The politics.txt file you created with news headlines. The finetune.json dataset you created for the Alpaca template. A link to the public Hugging Face Dataset repo for your finetune.json data file 

Public Hugging Face Dataset repo: https://huggingface.co/datasets/suman50/Fine_tune_dataset 

Fine-tune the Model 

A shared link to the notebook you used to fine-tune the LLM. The Hugging Face model repo for the final product. 

Co lab Notebook link: https://colab.research.google.com/#fileId=https%3A//huggingface.co/juntaoyuan/validate_chemistry_question/blob/main/Llama_3_1_8b_%2B_Unsloth_finetuning.ipynb Hugging Face model Repo: https://huggingface.co/bas369/finetune_model/tree/main 

Run an inference API server for the fine-tuned model 

The publicly accessible chatbot URL. A screenshot of the chatbot UI showing a relevant conversation 
