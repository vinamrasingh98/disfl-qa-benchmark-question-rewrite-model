# Disfl-qa-benchmark-question-rewrite-model

This project presents the development of a question rewrite model aimed at improving disfluency handling in the DISFL-QA benchmark dataset, a derivative of SQuADv2 that introduces contextual disfluencies to challenge existing Question Answering (QA) systems. We implemented and evaluated sequence-to-sequence models—BART, T5, and Flan-T5—designed to convert disfluent questions into fluent ones. The models were fine-tuned on the DISFL-QA dataset, with Flan-T5 demonstrating the highest performance, achieving BLEU and BERT F1 scores of 90.54 and 0.99, respectively.


## Requirements

+ PyTorch == 2.4.0+cu121
+ Transformers == 4.42.4
+ Evaluate == 0.4.2
+ Sacrebleu == 2.4.3
+ Bert-score == 0.3.13
+ datasets == 2.21.0
+ bertviz == 1.4.0
+ optuna == 3.6.1

## Dataset
[Disfl-QA: A Benchmark Dataset for Understanding Disfluencies in Question Answering](https://github.com/google-research-datasets/disfl-qa)
## Steps to Run 

STEP 1: Install the above packages mentioned

STEP 2: Follow the steps mentioned in the .ipynb notebook to run the inference code

##### Note
1. The model performace on train and validation dataset is present in flant5_train.ipynb.
2. The dataset files should be in the parent directory.
3. If using holdout datasets, rename the holdout dataset file as test.json.
4. All the datasets should follow .json extension.
5. Model is pretrained and uploaded to a private hugging face library which can be run by the private token mentioned in the flant5_inference file.
6. Use flant5_inference.ipynb notebook for running test and other holdout datasets.
7. Use flant5_train.ipynb notebook for finetuning the pretrained flant5 model.
8. Use optuna_hyperparameter_tuning.ipynb notebook for finding the optimized learning rate and weight decay parameters.
9. Use bertviz_view.ipynb notebook to vizualize the attentions heads of the model.
