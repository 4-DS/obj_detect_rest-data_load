![interface data_load](./imgs/data_load_inteface.drawio.png)

# Step CV-Pipeline: data_load [RU](README_RU.md)

Designed for loading data from various sources
In this example, it loads the dataset [`COCO`](http://images.cocodataset.org/).   
To launch and run cv-pipeline faster, we use the validation part of the dataset (~1 GB)
http://images.cocodataset.org/zips/val2017.zip
and annotations to them http://images.cocodataset.org/annotations/annotations_trainval2017.zip          
> If desired, you can use the full COCO dataset by specifying the link "http://images.cocodataset.org/zips/train2017.zip" 
to it in the configuration file ./params/step_params.json (или использую файл ./params/step_params_full.json)
    
Created based on [template](https://github.com/4-DS/step_template).
In order not to forget about the required cells in each laptop, the easiest way to create new jupyter notebooks is simply by copying [`substep_full.ipynb`](https://github.com/4-DS/step_template/blob/main/substep_full.ipynb) from standard [template](https://github.com/4-DS/step_template).
    
The final output of this step CV-Pipeline is two external storage urls
- **images**     
images of the downloaded dataset (saved as spark parquets)
- **annotations**    
annotation files of the downloaded dataset

## How to run a step CV-Pipeline: data_load

### Create a directory for the project (or use an existing one)
```
mkdir yolox_mmdet
cd yolox_mmdet
```  

### clone the repository: data_load
```
git clone --recurse-submodules https://gitlab.com/yolox_mmdet/data_load.git {data_load}
cd model_train
```  

### run step CV-Pipeline:data_load
```
python step.dev.py
```  
or
```
step.prod.py
``` 