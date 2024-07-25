# Week 2 Project: Monitoring distribution shift

```
pip install -e .
```

This project will have learners monitor deep learning systems for distribution shift using their predictions.

### Download dataset

In your terminal, please run
```
pip install gdown
```
Then, run the following:
```
gdown --id 1hdwWYFNJiCI_zFHWTMce6TETyj20GHG9
```
This will download a 3gb file of precomputed text embeddings to a file `data.zip`. Unzip the file and replace `monitor_project/data` with the unzipped folder. 


### Results
Results of evaluation of original model:
- en: {"loss": 0.2849099636077881, "acc": 0.8857421875}
- es: {"loss": 1.1791232824325562, "acc": 0.54248046875}

Results of evaluation of updated model:
- en: {"loss": 0.2905970513820648, "acc": 0.884765625}
- es: {"loss": 0.5415778756141663, "acc": 0.72802734375}

After the patch, the accuracy on the spanish data increased from 0.54 to 0.72