Here are two notebooks:
- finetune.ipynb: This is used to finetune on either pretrained indic bert or indic bert pretrained on the constraint dataset. THe variables that needs to be changed are model_num and lab_num. Change model_num to:
    - 0: to use the pre trained indicbert
    - 1: to use indicbert pretrained on constraint dataset. Make sure to pretrain it before 
  
  The lab num can be changed to:
    - 0: fake
    - 1: hate
    - 2: defamation
    - 3: offensive
    - 4: for coarse grained classification
- result.ipynb: It is used to create the temporary labels. THe variables that needs to be changed are       lab_num and EPOCH_NUM. lab_num is similar to lab_num in finetune.ipynb. EPOCH_NUM is the epoch number of a particular label. Choose the best epoch seen in the last notebook.