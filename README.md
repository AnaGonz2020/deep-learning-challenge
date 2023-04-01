# deep-learning-challenge
**Module 21 Challenge**

**Ana Gonzalez**

**Repo Files**
 * README - ReadMe file for module 21 Challenge and Analysis report for Alphabet Soup
 * Deep_Learning_Challenge Folder - 
     * AlphabetSoup_Funding_preoptimization.ipynb - initial model for Alphabet Soup data
     * AlphabetSoup_Funding_Optimized.ipynb - optimized model achieving 78% accuracy
     * Resources Folder:
        * charity_data.csv - file containing data
        * AlphabetSoupCharity_Optimization.h5
        * AlphabetSoupCharityOptimized_model.h5

# Step 4

*Overview of the analysis*: 
 - The purpose of this analysis is to assist Alphabet Soup, a non-profit foundation, in their funding of applicants with the best chance of success in their ventures. With the dataset that contains 34,000 organizations, we will create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.


**Results:** 
1. Data Preprocessing
    * What variable(s) are the target(s) for your model? 
    ---
        ** Our target variable is `IS_SUCCESSFUL` column, in order to process the data accordingly.
    ---
    * What variable(s) are the features for your model?
    ---
        ** For this data, we utilized the remaining columns as our determining features - `Application Type`, `Affiliation`, `Classification`, `Use Case`, `Organization Status`, `Income Amount`, `Special Considerations` and `Ask Amount`.
    ---
    * What variable(s) should be removed from the input data because they are neither targets nor features?
    ---
         ** For the initial testing and traing of the data, we removed both the columns `EIN1` and `NAME`
<br></br>

**Compiling, Training, and Evaluating the Model**
1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
---
     ** I used a total of 3 layers, both in the initial testing/training, as well as in the optimization steps. Initially, our model is testing at an accuracy of 72%. In altering the number of neurons, the optimized model began showing a higher accuracy of 78%.
---
2. Were you able to achieve the target model performance?
---
    ** In the initial trails, the highest accuracy I was achieving was 72%. Once optimization was put in place in a secondary jupyter notebook, I was able to reach an accuracy of 78%.
---
3. What steps did you take in your attempts to increase model performance?
---
    ** In order to obtain a higher accuracy score, I attempted 3 different methods for optimization. I initially attempted converting my model into a TensorFlow Lite converter, however, the sata proved to be difficult to process using this technique.  

    I went ahead and attempted to optimize the model by simply adjusting just the layer information, i.e.- number of units, activation argument, ect., however, this did not garner the results I was looking for.

    My final attempt, I went ahead and adjusted the dataset, instead of eliminating the `EIN1 and `NAME` columns, I only dropped the EIN column. This allowed me to optimize my model and increment my accuracy to 78%.
---
<br></br>

**Summary:** 
 - I was able to improve the model accuracy from 72% to 78% by adjusting the columns we take in when testing/training the model. Initially, I would have suggested potentially utilizing a different model, since the accuracy was not improving unless the data is manupilated a bit different, but after optimizing the model and adjusting the data taken in, this model would definitely help Alphabet Soup in their funding ventures.
