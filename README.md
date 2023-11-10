![interface data_load](./imgs/data_load_inteface.drawio.png)

# Step CV-Pipeline: data_load [RU](README_RU.md)

This component of the computer vision pipeline is responsible for loading data from various sources. It ensures the retrieval and preparation of data for further processing and analysis.    
It includes the following steps:   
- Source selection: This step involves choosing the source from which to load the data. The sources can be image or video files.     
- Data retrieval: After selecting the source, the computer vision component performs operations to retrieve data from the chosen source. For example, for image or video files, this may involve reading the files from disk.     
- Data transfer to the next stage of the pipeline: After loading and preparing the data, this step of the CV pipeline transfers it to the next stage of the pipeline, which includes other analysis and processing operations.    

In this example, it loads the dataset [`COCO`](http://images.cocodataset.org/).   
To launch and run cv-pipeline faster, we use the validation part of the dataset (~1 GB)
http://images.cocodataset.org/zips/val2017.zip
and annotations to them http://images.cocodataset.org/annotations/annotations_trainval2017.zip          

    
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
git clone --recurse-submodules https://github.com/4-DS/obj_detect-data_load.git {data_load}
cd {data_load}
```  

### run step CV-Pipeline:data_load
```
python step.dev.py
```  
or
```
step.prod.py
``` 