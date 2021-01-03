# IREL_IIIT @ constraint-aaai

This repository contains our code for our submission at Constraint Hindi Hostility detection shared task. It contains 4 parts which needs to performed sequentially as follows:
- Preprocessing: Preprocessing the tweets and extracting emojis, hashtags, etc. It is present in the [preprocessing][1] directory.
- Pretraining: Continued pretraining of indicbert on the provided dataset. It is present in the [pretraining][2] directory.
- Finetuning: Finetuning the transformer model to downstream classification task. It is present in the [finetuning][3] directory
- Result Generation: Genrating the csv files for final submission. It is present in the [results_gen][4] directory.

Further information about each part can be found in the respective directories.

Other folders include:
- [temp][5]: It will contain the temporary files created while running the model.
- [data][6]: It contains the dataset.

[1]: preprocessing
[2]: pretraining
[3]: finetuning
[4]: results_gen
[5]: temp
[6]: data
