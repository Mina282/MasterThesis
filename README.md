# MasterThesis
Code for IMPROVING LEXICAL DIVERSITY OF DOMAIN-SPECIFIC AUTOMATIC TEXT GENERATION WITH OUT-OF-DOMAIN TRAINING DATA AND STYLE CONDITIONING, master’s thesis by Mina Shahmoradi, Tampere University, November 2025. 

Overview of purpose

Style conditioning strategies to combine out of domain data to in domain data with the aim to increase language diversity of the generated output while maintaining the stylistic differences.

Description

This thesis addresses the problem of limited vocabulary in CDS text generation, where the loss in diversity results from tail truncation taking place in training of statistical generative models. To address the problem, the study examines the incorporation of out-of-domain texts (children’s book texts, CBT) into CDS text generation to enrich the vocabulary. The work first evaluates three alternative style conditioning strategies in LM training and generation to allow use of multi-domain training data while supporting text generation in a desired style. Experimental results demonstrate that all style conditioning methods successfully maintained key CDS characteristics during text generation, such as utterance length, syntactic simplicity, and part-of-speech distributions. However, these methods alone did not increase the lexical diversity of the generated output, indicating that style conditioning itself does not enable effective transfer of out-of-domain vocabulary into CDS-style output.


Dependencies
1. Python
1.1. For LM training:
•	tensorflow==2.12.1
•	tensorflow-text==2.12.0
1.2. For evaluation of the generated text data:
•	evaluate (https://huggingface.co/docs/evaluate/en/installation)
•	stanza (https://stanfordnlp.github.io/stanza/)
•	matplotlib
•	pandas
•	scipy

Instructions for text generation and analysis
After downloading childesr https://github.com/langcog/childesr and children’s book text https://www.gabormelli.com/RKB/Children%27s_Book_Test_(CBT)_Dataset
Each of different conditioning strategies main can be used to combine training and train the language model data accordingly.

Run S1_main.py/ S1_main.py / S1_main.py  to train the model and generate transcripts with it (after setting data paths inside the file). 

Run compare_datasets.py to extract linguistic features for the given texts (or collections of texts):
The same code give a possibility to check statistical significance of feature changes along with (1) an age of a target child and (2) a number of words in a collection of texts corresponding to an age bin.

Run analyze_results.m to plot the feature comparison of the generated transcripts against original transcripts (set input and output paths inside the file).

Acknowledgments
This thesis has been built upon previous study: Räsänen & Kocharov (2024). "A Pipeline for Stochastic and Controlled Generation of Realistic Language Input for Simulating Infant Language Acquisition". 
https://github.com/SPEECHCOG/GILES_pilot/

