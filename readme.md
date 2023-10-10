1. 解决request访问权限问题, huggingface.co网络访问权限未解决，可用手动下载方法代替    
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
> * glue: https://huggingface.co/datasets/glue/blob/main/glue.py  下载完之后，放到固定位置$glue_path，修改代码  raw_datasets = load_dataset(glue_path, task_name, cache_dir=cache_dir)
> * mnli: https://dl.fbaipublicfiles.com/glue/data/MNLI.zip



> git学习视频：https://www.bilibili.com/video/BV1r3411F7kn/


**windows conda 环境安装**    
* conda create -n compress python=3.8    
* **conda安装pytoch2.1：** conda install pytorch torchvision torchaudio pytorch-cuda=11.8 -c pytorch -c nvidia    
* **pip安装pytoch2.1：**  pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118    
* 


