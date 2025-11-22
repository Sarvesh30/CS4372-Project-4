# CS4372-Project-4

The code can be run with 'Assignment 4 Code CS 4372 Final Submission.ipynb'
All text was scraped publicly from the link: https://www.gutenberg.org/cache/epub/1513/pg1513.txt

1) Import Modules and Load/Clean Data
   - In this project, we used the following notable modules:
       - requests and textwrap were used to load and visualize the text
       - transformers library was used for pipeline development, tokenization, and loading models
       - peft library was used for tasks associated with LoRA (Low-Rank Adaptation)
    - The text was chunked to be compatible with pre-trained models
2) Creating Q&A Pairs
   - To fine tune the DistlledBERT model, 120 Q&A pairs from Act 1-3 of Romeo and Juliet were created
   - The 120 Q&A pairs include questions, answers, and context for 15 different chunks
3) Baseline Pre-Trained Transformer
   - The Q&A chunks were split into training/testing chunks to avoid data leakage and to evaluate performance on unseen Q&A pairs
   - The pre-trained DistilledBERT model was used as a baseline to evaluate performance of the Q&A system using metrics such as EM, F1, and sentiment scores from a pre-trained all-MiniLM-L6-v2 model.
4) Fine-Tuned Transformer with LoRA
   - The Q&A pairs were utilizied in fine-tuning the DistilledBERT pre-trained model with LoRA
   - The fine-tuned transformer was evaluated using EM, F1, and sentiment scores.
5) Hypertuning the Fine-Tuned Transformer (IN PROGRESS)
   - The fine-tuned transformer is being hypertuned with learning rate and LoRA parameters to strengthen model performance


  
