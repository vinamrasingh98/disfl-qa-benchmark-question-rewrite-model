# Disfl-qa-benchmark-question-rewrite-model

The project is facial-expression-recognition system using ResNext to identify a person's emotions and send mood feedback report/detailed mood analysis report to make him/her joyful. The project classifies the person’s emotions into five categories: happy, sad, angry, surprised, and neutral. For more detail you can refer our research paper: [EmotionNet: ResNeXt Inspired CNN Architecture for Emotion Analysis on Raspberry Pi](https://ieeexplore.ieee.org/document/9573569)

The classifier network was trained on the FERPlus dataset. An interactive GUI platform was designed using KivyMD to control the overall system. 


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
1. The dataset files should be in the parent directory.
2. If using holdout datasets, rename the holdout dataset file as test.json.
3. All the datasets should follow .json extension.
4. Model is pretrained and uploaded to a private hugging face library which can be run by the private token mentioned in the flant5_inference file.
5. Use flant5_inference.ipynb notebook for running test and other holdout datasets.
6. Use flant5_train.ipynb notebook for finetuning the pretrained flant5 model.
7. Use optuna_hyperparameter_tuning.ipynb notebook for finding the optimized learning rate and weight decay parameters.
8. Use bertviz_view.ipynb notebook to vizualize the attentions heads of the model.
