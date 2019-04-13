## Data Science MVP - v0.1

This is a basic data science project template intended to demonstrate how to use [cookiecutter-datascience](https://drivendata.github.io/cookiecutter-data-science/) for better project workflow and engineering practices.

In v0.1, we take a freshly initialized cookiecutter datascience project and remove the files that are likely to be unfamiliar to new data scientists, leaving only the ones that present a self-describing project workflow.

## How to use this template (v0.1)

Use `notebooks/mvp.ipynb` as a guide as you work through your Minimum Viable Product. Each section will guide you through one stage of a data science pipeline. I've structured this following the OSEMN (pronounced "awesome") paradigm of data science:

### **A**bstract
Take some time to think about what you want to do -- and practice describing your project -- before you dive into the code. I've added this step to the OSEMN workflow because  I believe that the preliminary design phase is important enough to earn a formal place.
### **O**btain
Find the data that will help you achieve the goals of your design. Don't do anything with it yet; save a copy of the data in its raw state. Take some time to write some notes about where you found it, what information it contains, and how you expect it to answer your question. 
### **S**crub
Look through the raw data files and see what you will need to do to them in order to have a workable data set. If your source data is already well-formatted, you may want to ask yourself why it hasn't already been analyzed and what other people may have overlooked when they were working on it. Are there other data sources that might give you more insights on some of the data you have here? The end goal of this step is to produce a design matrix, containing one column for every variable that you are modeling, including a column for the outputs, and one row for every observation in your data set. It needs to be in a format that won't cause any problems as you visualize and model your data.
### **E**xplore
Before you start exploring the data, write out your thought process about what you're looking for and what you expect to find. Take a minute to confirm that your plan actually makes sense. Calculate summary statistics and plot some charts to give you an idea what types of useful relationships might be in your dataset. Use these insights to go back and download additional data or engineer new features if necessary. Not now though... remember we're still just trying to finish the MVP!
### **M**odel
Perform a train/validate/test split on your data. Handle class imbalances if you need to. Build and train your models. Save the models for future use. Write a simple program that loads your model and uses it to make predictions -- think of how your end users might want to apply your model. Does it do what it's supposed to do? How easy is it to use?
### i**N**terpret
How well does your model perform? How do we know what "good" performance is? How well do humans perform at this task? What kinds of observations are more difficult for it to predict correctly? Difficult problems usually don't have right or wrong answers. How well can you explain your results?

## Get it to work, then get it to work right.

When working through the notebook, remember that the purpose of the MVP is not to put together a solution that's ready to be published! This is your chance to take a quick pass through the data, run it through a simple model, and get some preliminary results. When this phase is over, you'll have an end-to-end pipeline and a basic understanding of the problem. Then you'll be able to iterate on each stage as you improve your research and find better and better insights.

## Turning the MVP into a working pipeline

At the start of each code cell there is a `%%writefile` command that is commented out twice. When you're done building your MVP, uncomment these lines and run the cells again. (Remember to run the entire notebook once before doing this to make sure that your code works!) These commands will export your code cells to python scripts in the `src` directory. The last cell will build a `main.py` script in the top level directory that can be run to execute the entire pipeline.

Note that for this to work, you'll either need to include your import statements in the code cells where they're used, or you'll need to go through the generated scripts manually and make sure they have everything they need to run. You will also need to be careful about sharing variable names across cells, since they won't be accessible when the code is exported to separate scripts. Work with these cells as if each one is an independent Python script.

_In this version (0.1), I've removed the files from cookicutter datascience that would be useful for releasing your project as an installable package._


## Project Organization (modified from cookiecutter-datascience)
------------
```
    ├── LICENSE
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
```

--------
Removed files:

(See https://datasciencemvp.com for tutorials on how to integrate these with your projects. And drop me a comment if you're eager to get started with any of these and I haven't written a post about them yet. These tools may be unfamiliar to new data scientists, and the intention behind this version is to get you up and running as quickly as possible.)

```
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── data
    │   ├── external       <- Data from third party sources.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    |
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.testrun.org
```

Edited files:

```
    ├── src
        ├── data
        │   └── make_dataset.py  <- removed dependency on 'click' library
```

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
