# Spatial-Role-Labelling
This project aims to understand and implement techniques for spatial role labelling in radiology reports. This involves identifying spatial relations between spatial entities and spatial connectors mentioned in radiology reports.


## Method

1. **Get three vectors from BERT.**
   - [CLS] token vector
   - averaged entity_1 vector
   - averaged entity_2 vector
2. **Pass each vector to the fully-connected layers.**
   - dropout -> tanh -> fc-layer
3. **Concatenate three vectors.**
4. **Pass the concatenated vector to fully-connect layer.**
   - dropout -> fc-layer

## Running

```bash
$ python3 main.py --do_train --do_eval
```
## Prediction

```bash
$ python3 predict.py --input_file {INPUT_FILE_PATH} --output_file {OUTPUT_FILE_PATH} --model_dir {SAVED_CKPT_PATH}
```

