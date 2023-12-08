Use the following README template to create your README file. 

A well-written README file is crucial for other people to properly understand what you have done in your project.

Note:  The quality of your repository (e.g., content, organization, reproducibility, transparency) will directly reflect on your final grade. This applies to the README file too. 

# Group Name

_Here, you should provide a group name you want to be referred to as, as well as the names (and optionally contact info) of all group members. Additionally, define a group leader, i.e. one person in your group that is the primary contact if tutors want to communicate with your group. Also mention here which tutor is assigned to your project._

_Example:_

-   _Group name:_
    
-   _Group code:_
    
-   _Group repository:_
    
-   _Tutor responsible: _
    
-   _Group team leader:_
    
-   _Group members:_


  
## Setup instructions 
Explain how we can run your code in this section. 
Have you used libraries that were not included in the conda environment 'dnlp' which we provided? 
If so, write down the exact installation instructions or provide an .sh file for the installation.

Which files do we have to execute to train/evaluate your models? 
We should be able to reproduce the results you've obtained. 

Hint: At the end of the project you can set up a new environment and follow your setup instructions making sure  they are sufficient and if you can reproduce your results. 

## Methodology
In this section explain what and how you did in your project. 

Describe briefly the ideas that you implemented to improve the model. Make sure to indicate how are you using existing ideas and extending them.

## Experiments
Keep track of your experiments here. 
Write down all the main experiments you did even if they didn't yield an improved performance. 
We expect that you write down at least your baseline implementation and for each task one experiment which improved the models performance on this task. 
Of course, you can add include more experiments.

For each experiment answer briefly those questions:

- What were your expectations for this experiment?
- What have you changed compared to the base model (or to previous experiments, if you run experiments on top of each other)?
-  How to run the experiment? 
Write down the command which you used to execute the experiment. We should be able to reproduce the experiment.
- What were the results?
 Add relevant metrics and plots that describe the outcome of the experiment well. 
Discuss the results as well. Why did improvement A perform better/worse compared to other improvements? Did the outcome match your expectations? Can you recognize any trends or patterns?


## Visualizations 
Add relevant graphs of your experiments here. Those graphs should show relevant metrics (accuracy, validation loss, etc.) during the training. Compare the  different training processes of your improvements in those graphs. 
For example, you could analyze different questions with those plots like: 
-Does improvement A converge faster during training than improvement B? 
-Does Improvement B converge slower but perform better in the end? 
-etc...

## Results 
Summarize all the results of your experiments in a table:

|                |SST               |QQP            |STS                        | Paraphrase detection | Paraphrase Generation
|----------------|-----------|------- |---------|----|-----------------------------|
|Experiment 1 |45.23%           |...            | ...|...|...
|Experiment 2          |58.56%            |...           |...|...|...
|Experiment 3        |52.11%|...|...|...|...
|...        |...|...|...|...|...
## Hyperparameter Optimization 
Describe briefly how you found your optimal hyperparameter. If you focussed strongly on Hyperparameter Optimization, you can also include it in the Experiment section. 

Note: Reinforce random parameter optimization with no motivation/discussion is not interesting and will be graded accordingly
## Members Contribution 
Explain what member did what in the project:

Member 1: _implemented the training objective using X, Y, and Z. Supported member 2 in refactoring the code. Data cleaning, etc._

Member 2: ...

...

We should be able to understand each member's contribution within 5 minutes. 

## References 
Write down all your references (other repositories, papers, etc.) that you used for your project.