# Alzheimer-claasification-task
 all the code has successfully run in the kaggle platform.
 
Since the maximum running time allowed on the Kaggle platform is 12 hours, 
 when attempting to reproduce, it is necessary to save the log of each run result and import it into a new notebook to continue running from the last breakpoint.

## Code Guide
To facilitate easy reproduction and code review, the pipeline is divided into distinct Jupyter Notebooks. Readers can navigate directly to the specific stage of the methodology they wish to examine:

* 📄 **`Data-augmentation.ipynb`**
  Contains the data preprocessing pipeline. Since the original dataset link on Kaggle is no longer available, this code can no longer be executed. It is provided solely to demonstrate the details of the data augmentation process.

* 📄 **`random-search-25-times.ipynb`**
  The implementation of the Random Search hyperparameter tuning baseline. It logs the search history across 25 independent trials.
