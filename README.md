# Improving autism identification with multisite data via site-dependence minimisation and second-order functional connectivity

## Requirements
numpy  
pandas  
scipy  
scikit-learn  
nilearn  
networkx
## Download required packages
```
pip install -r requirements.txt
```
## Download and preprocess ABIDE data
In the files ``train.py``, ``preprocess_data.py`` and ``fetch_data.py``, change 'path/to/data/' to an appropriate file path.
To download the ABIDE data, run:
```
python fetch_data.py
```
Options are available for the preprocessing pipeline, brain atlas and functional connectivity. Run `python fetch_data.py --help` for information about the available options. For tangent connectivity, see below.

## Classification
The default model provided is the MIDA model with tangent pearson functional connectivity trained with a ridge classifier and evaluated with 10 fold CV. Can be run by:
```
python run_model.py
```
The default functional connectivity here is tangent pearson and is computed at run time separately for train and test folds. As above, run `python run_model.py --help` to see the available options.
