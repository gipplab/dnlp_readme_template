Use the following README template to create your README file. 

A well-written README file is crucial for other people to properly understand what you have done in your project.

Note:  The quality of your repository (e.g., content, organization, reproducibility, transparency) will directly reflect on your final grade. This applies to the README file too. 

# Group Name

Here, you should provide a group name you want to be referred to as, as well as the names (and optionally contact info) of all group members. Additionally, define a group leader, i.e. one person in your group who is the primary contact if tutors want to communicate with your group. Also, mention here which tutor is assigned to your project.

_Example:_

-   **Group name:**
    
-   **Group code:**
    
-   **Group repository:**
    
-   **Tutor responsible:**
    
-   **Group team leader:**
    
-   **Group members:**

  
# Setup instructions 
Explain how we can run your code in this section. We should be able to reproduce the results you've obtained. 

In addition, if you used libraries that were not included in the conda environment 'dnlp' explain the exact installation instructions or provide a ```.sh``` file for the installation.

Which files do we have to execute to train/evaluate your models? Write down the command which you used to execute the experiments. We should be able to reproduce the experiments/results.

_Hint_: At the end of the project you can set up a new environment and follow your setup instructions making sure they are sufficient and if you can reproduce your results. 

# Methodology
In this section explain what and how you did your project. 

If you are unsure how this is done, check any research paper. They all describe their methods/processes. Describe briefly the ideas that you implemented to improve the model. Make sure to indicate how are you using existing ideas and extending them. We should be able to understand your project's contribution.

# Experiments
Keep track of your experiments here. What are the experiments? Which tasks and models are you considering?

Write down all the main experiments and results you did, even if they didn't yield an improved performance. Bad results are also results. The main findings/trends should be discussed properly. Why a specific model was better/worse than the other?

You are **required** to implement one baseline and improvement per task. Of course, you can include more experiments/improvements and discuss them. 

You are free to include other metrics in your evaluation to have a more complete discussion.

Be creative and ambitious.

For each experiment answer briefly the questions:

- What experiments are you executing? Don't forget to tell how you are evaluating things.
- What were your expectations for this experiment?
- What have you changed compared to the base model (or to previous experiments, if you run experiments on top of each other)?
- What were the results?
- Add relevant metrics and plots that describe the outcome of the experiment well. 
- Discuss the results. Why did improvement _A_ perform better/worse compared to other improvements? Did the outcome match your expectations? Can you recognize any trends or patterns?

## Results 
Summarize all the results of your experiments in a table:

| **Stanford Sentiment Treebank (SST)** | **Metric 1** |**Metric n** |
|----------------|-----------|------- |
|Baseline |45.23%           |...            | 
|Improvement 1          |58.56%            |...          
|Improvement 2        |52.11%|...|
|...        |...|...|

| **Quora Question Pairs (QQP)** | **Metric 1** |**Metric n** |
|----------------|-----------|------- |
|Baseline |45.23%           |...            | 
|Improvement 1          |58.56%            |...          
|Improvement 2        |52.11%|...|
|...        |...|...|

| **Semantic Textual Similarity (STS)** | **Metric 1** |**Metric n** |
|----------------|-----------|------- |
|Baseline |45.23%           |...            | 
|Improvement 1          |58.56%            |...          
|Improvement 2        |52.11%|...|
|...        |...|...|

| **Paraphrase Type Detection (PTD)** | **Metric 1** |**Metric n** |
|----------------|-----------|------- |
|Baseline |45.23%           |...            | 
|Improvement 1          |58.56%            |...          
|Improvement 2        |52.11%|...|
|...        |...|...|

| **Paraphrase Type Generation (PTG)** | **Metric 1** |**Metric n** |
|----------------|-----------|------- |
|Baseline |45.23%           |...            | 
|Improvement 1          |58.56%            |...          
|Improvement 2        |52.11%|...|
|...        |...|...|


- Stanford Sentiment Treebank (SST)
- Quora Question Pairs (QQP)
- Semantic Textual Similarity (STS)
- Paraphrase Type Detection (PTD)
- Paraphrase Type Generation (PTG)

  
Results should have three-digit precision.
 

### Hyperparameter Optimization 
Describe briefly how you found your optimal hyperparameter. If you focussed strongly on Hyperparameter Optimization, you can also include it in the Experiment section. 

_Note: Random parameter optimization with no motivation/discussion is not interesting and will be graded accordingly_

## Visualizations 
Add relevant graphs of your experiments here. Those graphs should show relevant metrics (accuracy, validation loss, etc.) during the training. Compare the  different training processes of your improvements in those graphs. 

For example, you could analyze different questions with those plots like: 
- Does improvement A converge faster during training than improvement B? 
- Does Improvement B converge slower but perform better in the end? 
- etc...

## Members Contribution 
Explain what member did what in the project:

**Member 1:** _implemented the training objective using X, Y, and Z. Supported member 2 in refactoring the code. Data cleaning, etc._

**Member 2:** ...

...

We should be able to understand each member's contribution within 5 minutes. 

# References 
Write down all your references (other repositories, papers, etc.) that you used for your project.


# Frequent Asked Questions
Please add all FAQ you can think here (Talk with other hiwis to collect some nice questions)
