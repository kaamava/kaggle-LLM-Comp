# kaggle-LLM-Comp
#This is a repository which is used for store and remind me of the code and approach used for 2023.10 kaggle LLM competition. This will also contribute to my portfolio and application. 

LLM_train.ipynb  Model training code
LLM_infer.ipynb  Model infering code
llama_finetune.ipynb  llama model fine-tuning reference

Note: It is recommended to use GPU A100 to train the model. The model training time is approximately 6 hours.

Download open source data source(required):
https://www.kaggle.com/datasets/cdeotte/60k-data-with-context-v2

1. This competition is based on Wikipedia reading comprehension data and aims to develop a model for automatically answering multiple-choice questions. It is a typical multi-class classification problem, and to evaluate the accuracy of prediction results, the competition uses MAP@3 as the evaluation metric.

2. This competition provides correct answers for only 200 questions and does not provide reference articles. Therefore, participants need to search for additional training data to achieve better model performance. We generated 60,000 training samples by using the original Wikipedia texts and the GPT-3.5 model.

3. Since the competition does not provide the original texts, which contain a significant amount of useful information, we adopted a sentence vector approach. We measured the similarity between the prompt and the original Wikipedia texts to extract the most similar original text, which serves as the primary reference for the questions.

4. Based on the original text, prompt, options, and correct answers, we encoded the input using DeBERTa-v3-large and built a reading comprehension model using the AutoModelForMultipleChoice model from the Transformers library. When our model answers multiple-choice questions automatically, we first match the prompt and options with the original text and then use the model to predict the correct answer. Our model achieved a MAP@3 of 0.906 on the test set and ranked in the top xx% in the competition.

5. During the competition, we made efficient use of the competition time, controlled the pace effectively, engaged in active discussions, and formulated reasonable tasks for model iteration. We also organized brainstorming sessions to drive the progress of the competition. Meanwhile, we worked on model development to ensure the highest possible prediction accuracy.
![image](https://github.com/kaamava/kaggle-LLM-Comp/assets/106901273/cbe3ae98-8264-47ae-9b9f-b5dd80a45bf8)

![image](https://github.com/kaamava/kaggle-LLM-Comp/assets/106901273/fd97ba12-2b3a-4c08-bba6-8a3a385ccf65)
