# Applied ML HW2

## Collaborator:

- Yanlin Duan
- Chenchao Zang

## Instruction:
https://docs.google.com/document/d/1EHyWR-GZfwK5a9JJc_nFy3yvVofA11cMjvH7vXE6JH0/edit

## Framework
### Feature Selection

  * Drop features whose values are almost identical -- they are not providing enough information
  
  * By trail-and-error, we set up the threshold at 90%
  
  * Remove the banned feature which may lead information leakage. This includes:
  
    - rent information
    
    - household information
    
    - other labels that may leak the above two
   
### Imputation

  * Categorical Data: Most Frequent Value

  * Numerical Data: Median

  * One-Hot-Encoding:

    * LabelEncoding based on the raw dataset to create a generative framework

    * Do one-hot-encoding for trainning dataset and test dataset respectively based on the main framework just created
    
  * Special Case Handle: variable "uf64"
  
    * Create an indicator column for the missing and nonmissing values
    
    * Impute the missing values based on the median of observations with exclusion of "Not Applicable (9999)"

### Model Selection

  * GridCV to select parameter values
