1. 解决request访问权限问题    
* model = BertForSequenceClassification.from_pretrained(pretrained_model_name_or_path, num_labels=num_labels)   
> * 手动下载模型到C:\Users\wangbt\.cache\huggingface\hub\models--bert-base-uncased  下载地址[链接](https://huggingface.co/bert-base-uncased/tree/main)

* metric = load_metric('glue', task_name)
> * urllib3 (1.26.16) or chardet (5.2.0)  不行   
> * windows 
修改：C:\Windows\System32\drivers\etc    
增加：    
199.232.28.133 raw.githubusercontent.com      
> * linux    
sudo vim /etc/hosts    
199.232.28.133 raw.githubusercontent.com      

* raw_datasets = load_dataset('glue', task_name, cache_dir=cache_dir)
> * glue: https://huggingface.co/datasets/glue/blob/main/glue.py
> * mnli: https://dl.fbaipublicfiles.com/glue/data/MNLI.zip

> git学习视频：https://www.bilibili.com/video/BV1r3411F7kn/
