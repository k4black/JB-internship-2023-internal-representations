# JB-internship-2023-internal-representations


```shell
pip install pygit2 --prefer-binary
pip install torch==1.12.1+cu113 --extra-index-url https://download.pytorch.org/whl/cu113
pip install -U -r requirements.txt
```
    

1. Run job script 
    ```shell
    sbatch train.sh --base-model=Salesforce/codet5-small --config-name=test --postfix=2 --resume_training_id=... [other options]
    ```
2. Monitor status with 
    ```shell
    squeue -o "%.18i %.9P %.8j %.8u %.2t %.10M %.6D %.18R %p" | grep $USER
    squeue -o "%.18i %.9P %.8j %.8u %.2t %.10M %.6D %.18R %p" | grep gpu
    ```




sbatch train.sh --base-model=Salesforce/codet5-small --config-name=adamw --push-to-hub --save-model
