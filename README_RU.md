![interface data_load](./imgs/data_load_inteface.drawio.png)

# Step CV-Pipeline: data_load [EN](README.md)

Данный компонент CV(computer vision) пайплайна отвечает за загрузку данных из различных источников. Этот компонент обеспечивает получение и подготовку данных для дальнейшей обработки и анализа.    
Включает в себя следующие шаги:     
- Выбор источника данных: Этот шаг включает выбор источника, из которого необходимо загрузить данные.    
Источниками могут быть файлы изображений или видео.     
- Получение данных: После выбора источника компонент компьютерного зрения выполняет операции для получения данных из выбранного источника.        
Например, для файлов изображений или видео это может быть операция чтения файлов с диска.        
- Передача данных в следующий этап пайплайна: После загрузки и подготовки данных, данный шаг cv pipeline передает их в следующий этап pipeline, который включает другие операции анализа и обработки

В данном примере загружает датасет [`COCO`](http://images.cocodataset.org/).   
Для более быстрого запуска и прогона cv-pipeline используем валидационную часть датасета (~1 Гб)
http://images.cocodataset.org/zips/val2017.zip
и аннотации к ним http://images.cocodataset.org/annotations/annotations_trainval2017.zip          

    
Данный компонент создается из [шаблона](https://github.com/4-DS/step_template).
Чтобы не забывать про обязательные ячейки в каждом ноутбуке, проще всего создавать новые ноутбуки просто копированием [`substep_full.ipynb`](https://github.com/4-DS/step_template/blob/main/substep_full.ipynb) из стандартного [шаблона](https://github.com/4-DS/step_template) компоненты.
    
Конечным выходом работы данного step CV-Pipeline является два urls внешнего хранилища
- **images**     
изображения скачанного датасета (сохранен как spark parquets)
- **annotations**    
файлы аннотации скачанного датасета (сохранен как spark parquets)

## Как запустить шаг CV-Pipeline: data_load

### Создать директорию для проекта (или использовать уже существующую)
```
mkdir example_detector
cd example_detector
```  

### склонировать репозиторий data_load
```
git clone --recurse-submodules https://github.com/4-DS/obj_detect-data_load.git {data_load}
cd {data_load}
```  

### запустить шаг CV-Pipeline:data_load
```
python step.dev.py
```  
или
```
step.prod.py
``` 