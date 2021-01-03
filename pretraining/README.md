We have taken the run_language_modelling.py code from [allenai /
dont-stop-pretraining][1] repository.
We have used it to continue pretraining indicbert on the constraint dataset. In order to pretrain indicbert, at first, clone the repository from allenai
```
git clone https://github.com/allenai/dont-stop-pretraining
```
Then create the environment:
```
cd dont-stop-pretraining
conda env create -f environment.yml
conda activate domains
```
Then run the following code to pretrain your model:
```
python -m scripts.run_language_modeling --train_data_file ../../temp/tapt-corpus/texts.txt \
                                        --line_by_line \
                                        --output_dir "../../temp/tapt-models" \
                                        --model_type "ai4bharat/indic-bert" \
                                        --mlm \
                                        --per_gpu_train_batch_size 4 \
                                        --gradient_accumulation_steps 8  \
                                        --model_name_or_path "ai4bharat/indic-bert" \
                                        --do_train \
                                        --num_train_epochs 2  \
                                        --learning_rate 0.0001 \
                                        --logging_steps 50 \
                                        --block_size 128
```
The trained models will be saved [here][2]. Check the requirements [here][3]. In case if you face problems, install `transformers==2.10.0`

[1]: https://github.com/allenai/dont-stop-pretraining
[2]: ../temp/tapt-models
[3]: https://github.com/allenai/dont-stop-pretraining/blob/master/environment.yml