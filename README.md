## Title
Enhancing Alzheimer’s Disease Diagnosis through Automated Hyperparameter Optimization: A Bayesian Approach for EfficientNet Models

all the code has successfully run in the kaggle platform.
 
 Since the maximum running time allowed on the Kaggle platform is 12 hours, 
 when attempting to reproduce, it is necessary to save the log of each run result and import it into a new notebook to continue running from the last breakpoint.

## Code Guide
To facilitate easy reproduction and code review, the pipeline is divided into distinct Jupyter Notebooks. Readers can navigate directly to the specific stage of the methodology they wish to examine:

- 📄 **`Data-augmentation.ipynb`**  
  Contains the data preprocessing pipeline. Since the original dataset link on Kaggle is no longer available, this code can no longer be executed. It is provided solely to demonstrate the details of the data augmentation process.

- 📄 **`random-search-25-times.ipynb`**  
  The implementation of the Random Search hyperparameter tuning baseline. It logs the search history across 25 independent trials.  
  - Required input: The augmented dataset

- 📄 **`bo-25-times.ipynb`**  
  It contains the configuration for the Marginalized BO, executed over 25 iterations to discover the optimal hyperparameter bounds.  
Required input:
  - The augmented dataset  
  - Existing observational data (if re-running on Kaggle is required).

- 📄 **`standard bo-25-times.ipynb`**  
  It contains the configuration for the Standard BO, executed over 25 iterations to discover the optimal hyperparameter bounds.  
Required input:
  - The augmented dataset  
  - Existing observational data (if re-running on Kaggle is required).

* 📄 **`champion-analysis.ipynb`**  
  This notebook tests the best models ("Champions") found by each search strategy on the unseen test set. It loads the optimal hyperparameters, trains the final models, and outputs the detailed performance metrics (e.g., $98.69\%$ test accuracy for Standard BO vs. $98.80\%$ for Marginalized BO).

* 📄 **`champion-analysis-supplements.ipynb`**  
  This notebook supplements the code `champion-analysis.ipynb` by adding a set of standard BO hyperparameters that need to be trained and tested, then compared against existing stored results.

* 📄 **`plot-abo-slice1d.ipynb`**  
  Generates 1D slice visualizations of the Bayesian Optimization landscape and acquisition functions, providing mathematical insights into the optimization space explored by the models.
