# *MetaEval*: Measuring the Discrimination of Benchmarks for Efficient LLM

<img width="5610" height="2296" alt="framework" src="https://github.com/user-attachments/assets/e36f432d-6644-4776-8ae7-d0c8bd9f6647" />


**Contents**
1. Datasets
2. Dependencies
3. Run

--------------

<a name="1"></a>
## Datasets

All the datasets were obtained from our work "*Metaeval*" by
1. all_data/     → The complete raw dataset (all models, all questions, full softmax outputs, etc.)
2. data/         → The preprocessed and lightweight dataset ready for direct training/testing

<a name="2"></a>
## Dependencies

Python==3.9
PyTorch==1.13.0
attrs==23.2.0
joblib==1.3.2
jsonlines==4.0.0
numpy==1.26.4
scikit-learn==1.4.1.post1
scipy==1.12.0
setuptools==68.2.2
threadpoolctl==3.3.0
tqdm==4.66.2
wheel==0.41.2

## Run
resp_download_helper.ipynb — (optional) organize and preprocess the raw response data
model_mutidata.ipynb — (required) fit item discrimination parameters
estimate_theta.ipynb / estimate_theta_nodiscrim.ipynb — estimate model abilities and make performance predictions
split_discrim_bench.ipynb — split benchmarks according to discrimination or other specified rules
