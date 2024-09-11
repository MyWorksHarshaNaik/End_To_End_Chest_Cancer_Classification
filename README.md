# End_To_End_Chest_Cancer_Classification

## Dataset:
#### https://www.kaggle.com/datasets/mohamedhanyyy/chest-ctscan-images

### Step 1: Creating a template.py

```bash
python template.py
```

### Step 2: Install requirements.txt

```bash
pip install -r requirements.txt 
```

### Step 3: configure setup.py

### Step 4: setup src/cnnClassifier/__init__.py
#### --> creating a logger
#### --> Create a main.py
#### --> run a main.py

```bash
python main.py
```

### Step 5: setup src/cnnClassifier/utils/common.py
#### --> ConfigBox and ensure_annotations experiment in research/trials.ipynb

### Workflows
#### Update config.yaml
#### Update secrets.yaml [Optional]
#### Update params.yaml
#### Update the entity
#### Update the configuration manager in src config
#### Update the components
#### Update the pipeline
#### Update the main.py
#### Update the dvc.yaml

### Step 6:  research/01_data_ingestion.ipynb
#### --> update config/config.yaml
#### --> setting up data_ingestion
#### --> update params.yaml -> first add dummy values (key: val) 
#### --> create entity -> research/01_data_ingestion.ipynb -> class DataIngestionConfig
#### --> update src/cnnClassifier/constants/__init__.py 
#### --> update research/01_data_ingestion.ipynb 

### Step 7: modular coding
#### --> update src/cnnClassifier/entity/config_entity.py
#### --> update src/cnnClassifier/config/configuration.py
#### --> update src/cnnClassifier/components/data_ingestion.py
#### --> update src/cnnClassifier/pipeline/stage_01_data_ingestion.py
#### --> update main.py
#### --> delete the artifacts folder
#### --> Run main.py
```bash
python main.py
```
#### --> add 'artifacts/*' to gitignore

### Step 8:  research/02_prepare_base_model.ipynb
#### --> update config/config.yaml
#### --> Update params.yaml
#### --> Update research/02_prepare_base_model.ipynb


### Step 9: modular coding
#### --> update src/cnnClassifier/entity/config_entity.py
#### --> update src/cnnClassifier/config/configuration.py
#### --> update src/cnnClassifier/components/prepare_base_model.py
#### --> update src/cnnClassifier/pipeline/stage_02_prepare_base_model.py
#### --> update main.py
#### --> delete the artifacts folder
#### --> Run main.py
```bash
python main.py
```

### Step 10:  research/03_model_trainer.ipynb
#### --> update config/config.yaml
#### --> Update research/03_model_trainer.ipynb


### Step 11: modular coding
#### --> update src/cnnClassifier/entity/config_entity.py
#### --> update src/cnnClassifier/config/configuration.py
#### --> update src/cnnClassifier/components/model_trainer.py
#### --> update src/cnnClassifier/pipeline/stage_03_model_trainer.py
#### --> update main.py
#### --> delete the artifacts folder
#### --> Run main.py
```bash
python main.py
```

### Step 12:  research/04_model_evaluation_with_mlflow.ipynb

###  dagshub
[dagshub](https://dagshub.com/)

### Step 13: modular coding
#### --> update src/cnnClassifier/entity/config_entity.py
#### --> update src/cnnClassifier/config/configuration.py
#### --> update src/cnnClassifier/components/model_evaluation_mlflow.py
#### --> update src/cnnClassifier/pipeline/stage_04_model_evaluation.py
#### --> update main.py
#### --> delete the artifacts folder
#### --> Run main.py
```bash
python main.py
```