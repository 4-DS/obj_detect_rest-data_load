![interface data_load](./imgs/data_load_inteface.drawio.png)

### add sinara module  
```
git submodule add https://github.com/4-DS/sinara.git sinara
```  

### init DSML module  
```
git submodule init
```

### update to latest DSML module
```
git submodule update --remote --merge
```

# Step CV-Pipeline: data_load

Предназначен для загрузка данных из различных источников
В данном примере загружает датасет [`COCO`](http://images.cocodataset.org/).   
Для более быстрого запуска и прогона cv-pipeline используем валидационную часть датасета (~1 Гб)
http://images.cocodataset.org/zips/val2017.zip
и аннотации к ним http://images.cocodataset.org/annotations/annotations_trainval2017.zip          
> При желании можно использовать полный датасет COCO указав ссылку "http://images.cocodataset.org/zips/train2017.zip" на него в конфигурационном файле ./params/step_params.json (или использую файл ./params/step_params_full.json)
    
Данный компонент создается из [шаблона](https://github.com/4-DS/step_template).
Чтобы не забывать про обязательные ячейки в каждом ноутбуке, проще всего создавать новые ноутбуки просто копированием [`substep_full.ipynb`](https://github.com/4-DS/step_template/blob/main/substep_full.ipynb) из стандартного [шаблона](https://github.com/4-DS/step_template) компоненты.
    
Конечным выходом работы данного step CV-Pipeline является два urls внешнего хранилища
- **images**     
изображения скачанного датасета (сохранен как spark parquets)
- **annotations**    
файлы аннотации скачанного датасета (сохранен как spark parquets)
