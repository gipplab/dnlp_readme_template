This is an example of a poor README file from a group that did that project last year. 
<b> Why is that README not good? </b>

- No member's contribution is written down. Which member did what?
- No documentation of experiments at all, what was tried to improve the model's performance and why?
- No graphics/ visualizations of the experiments. 
- Most of the stuff that is written down in the requirements and evaluation section is boring/ unnecessary, because it's already explained in the provided project handout. 


<div align="center">

<h1> DNLP SS23 Final Project - Multitask BERT</h1>

</div>

  

In this repository you will find code for the final project of the the _M.Inf.2202 Deep Learning for Natural Language Processing_ course at the University of Göttingen. You can find the handout [here](https://1drv.ms/b/s!AkgwFZyClZ_qk718ObYhi8tF4cjSSQ?e=3gECnf).

  

In this project, important components of the BERT model are implemented.

Embeddings produced by our BERT model were used for three downstream tasks: sentiment classification, paraphrase detection and semantic similarity.

  

We implemented [a Multi-task learning methodology](METHODOLOGY.md) to improve the baseline model.

  

## Requirements

* Make sure you have Anaconda or Miniconda installed.

* Run [setup.sh](./setup.sh) to set up a conda environment and install dependencies:

```

source setup.sh

```

The setup.sh file contains the following:

```setup

#!/usr/bin/env bash

  

conda create -n dnlp python=3.8

conda activate dnlp

  

conda install pytorch==1.8.0 torchvision torchaudio cudatoolkit=10.1 -c pytorch

pip install tqdm==4.58.0

pip install requests==2.25.1

pip install importlib-metadata==3.7.0

pip install filelock==3.0.12

pip install sklearn==0.0

pip install tokenizers==0.10.1

pip install explainaboard_client==0.0.7

```

Activate the dnlp environment by running:

```

conda activate dnlp

```

Details of the environment so that used libraries and dependencies can be found in environment.yml file

  

## Training

Since the model is designed to perform three different NLP tasks, we train on three different datasets. More precisely, we use the [Standford Sentiment Treebank](https://nlp.stanford.edu/sentiment/treebank.html) (Socher et al., 2013), consisting of 11,855 single sentences from movie reviews extracted from movie reviews, to classify a text's sentiment. Further, we use the Quora dataset consisting of 400,000 question pairs to train for paraphrase detection. Lastly, we seek to measure the degree of semantic equivalence, using data from the SemEval STS Benchmark dataset consisting of 8,628 sentence pairs of varying similarity.

  

To train the model, run this command:

  

```

python -u multitask_classifier.py --option finetune --lr 1e-5 --batch_size 64 --local_files_only

```

or just run the provided [submit_train.sh](./submit_train.sh) file containing the command above using _sbash_.

  

```train

sbash submit_train.sh

```

>Note: The hyperparameters for our best model are already included in the above code snippets.

  

#### Disclaimer: We trained on a computer cluster provided by university IT infrastructure. You may run into issues with slow training speed when using commonly used hardware systems.

  

## Evaluation

  

The evaluation of the model is conducted after each epoch and done so automatically when training. The method _model_eval_multitask()_ imported from [evaluation.py](/evaluation.py) evaluates each epoch.

  

We evaluate each task separately and create a weighted metric summary for all

  

* Paraphrase Detection: Proportion of correctly classified paraphrase pairs

* Sentiment Classification: Proportion of correct classification of sentiment

* Semantic Textual Similarity: Pearson correlation coefficient of predicted and true values

* Best Metric: Weighted average of each tasks

  

## Pre-trained Models

  

For this project we used the so called [bert-base-uncased](https://huggingface.co/bert-base-uncased) pre-trained model implementation that loads pre-trained weights. Within the [multitask_classifier.py](./multitask_classifier.py) file we call the _from_pretrained()_ method from [base_bert.py](./base_bert.py) to retrieve the pre-trained model. In other words, when trying to run the training, you mind want to replace "finetune" to "pretrain", i.e.

```

python -u multitask_classifier.py --option pretrain --lr 1e-5 --batch_size 64 --local_files_only

```

  

  

## Results

  

Our model achieves the following performance on :

  

| Model  | Paraphrase Accuarcy  | Sentiment Accuracy | Semantic Text Similarity Correlation |

| ------------------ |---------------- | -------------- | --------------|

| Multitask Classifier BERT Model | 89.01% |  49.59% |  88.00%  |

  

During training, we create a text file with information about our best model from every epoch.

  

  

| Model  | Paraphrase Accuarcy  | Sentiment Accuracy | Semantic Text Similarity Correlation |

| ------------------ |---------------- | -------------- | --------------|

| Multitask Classifier pretrain BERT Model | 26.34% |  62.47% |  37.30%  |

  

For experiment we checked the model performance when setting it to 'pretrain' instead of 'finetune'. As expected the results were not satisfying, since we have freezed weights which are not updating the model can't learn efficiently and only task specific layers are updating weights.