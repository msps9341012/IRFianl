# IRFianl
## Prerequisite
* All codes are based on Google Colab with TPU. 
* The model weights (including .ckpt, vocab.txt, bert_config.json) and output should be stored on Google Cloud Storage.
* Also, upload the TLDR-19 testing set to your Google Cloud Storage.
## Intermediate-Task tuning
* Run Intermediate.ipynb, you change the task in the code.
* If you want to fine-tun QQP or QNLI, you should add the preprocess.py into run_classifier.py from bert's repo.
* If you want to fine-tune SQuAD 2.0, use the run_squad.py from bert's repo.
## Re-ranking
* Run ReRanking.ipynb and set INIT_CHECKPOINT to the ckpt filename that you get from intermediate task.
* The code includes training and evaluation on MARCO dev set and TLDR-19 eval set.
* For TLDR-19, download the predictions and use trec_eval to compute the metrics.

After training all models, run Embedding_Analysis.ipynb to get the embedding plots that is shown in the report.
