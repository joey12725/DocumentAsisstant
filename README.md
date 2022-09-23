# DocumentAsisstant
A chat bot that uses an OCR, an extractive summarization model, and GPT-3 to understand and respond to questions about large bodies of text. 

OCR is done using PyTesseract, PDF2Image and Pillow. This was origionally done with Textract, but I found that the added speed came at the cost of length constraints, exess infomation, and added cost. 

The summarization function is based on the Recall-Oriented Understudy for Gisting Evaluation (ROUGE) method of summarization (more specifically ROUGE-N), with added support for user input of keywords. This allows the user to ensure that the summary contains relevant information to the questions the user asks. 

Once the summarization is done, the user is prompted to provide their question, as well as a "creativity" score which determines the temperature of the GPT-3 request. The prompt goes through a little extra filtration, and then the request is sent.

This script also estimates costs before the request is sent, as well as informs the user of the true cost after. 
