# kaggle-otto-recsys

Code for trial to adapt Transformers4Rec on the kaggle competitions.

[Kaggle OTTO – Multi-Objective Recommender System](https://www.kaggle.com/competitions/otto-recommender-system)

[OTTO Recommender Systems Dataset](https://github.com/otto-de/recsys-dataset)

[NVIDIA-Merlin / Transformers4Rec](https://github.com/NVIDIA-Merlin/Transformers4Rec)

[NVIDIA-Merlin / NVTabular](https://github.com/NVIDIA-Merlin/NVTabular)

[NVIDIA-Merlin / core](https://github.com/NVIDIA-Merlin/core)

## Trial

With Google Colab Pro Plus Nvidia A100, it takes about 6 hours per 1 epoch to train kaggle otto dataset with full 1,855,603	items. And I tried to train with subset (657,940 items candidates from orders).

You should be careful the version of Transformers4Rec. I tried 0.1.15 and there are a lot of changes between 0.1.15 and 0.1.16

I recommend to start from the examples and tutorials of Transformers4Rec and NVTabular, Merlin / core.

## Official Examples

[Transformers4Rec Example Notebooks](https://github.com/NVIDIA-Merlin/Transformers4Rec/tree/main/examples)

[NVTabular Example Notebooks](https://github.com/NVIDIA-Merlin/NVTabular/tree/main/examples)

## Issues

I got help from below issues and comments.

[[BUG] getting wrong dimension from Triton as a response when serving a TF4Rec model with TorchScript #538](https://github.com/NVIDIA-Merlin/Transformers4Rec/issues/538)

[[QST] How/Where Is the Schema Generated? #271](https://github.com/NVIDIA-Merlin/Transformers4Rec/issues/271)

[[FEA] Model inference locally #359](https://github.com/NVIDIA-Merlin/Transformers4Rec/issues/359)

[[BUG] nvtabular never registered with registry torch.dataloader_loader while using transformers4rec #1713](https://github.com/NVIDIA-Merlin/NVTabular/issues/1713)

[[BUG] Cannot install with conda/pip on Ubuntu 20.04 #424](https://github.com/NVIDIA-Merlin/Transformers4Rec/issues/424)

[ModuleNotFoundError: No module named 'merlin.dag.executors' #1684](https://github.com/NVIDIA-Merlin/NVTabular/issues/1684)

[[FEA] How can it be extended to handle next basket recommendation ? #268](https://github.com/NVIDIA-Merlin/Transformers4Rec/issues/268)

[[QST] Binary Classification - Dataloaders #405](https://github.com/NVIDIA-Merlin/Transformers4Rec/issues/405)

[[QST] what is output predictions meaning? #594](https://github.com/NVIDIA-Merlin/Transformers4Rec/issues/594)

## schema Tag

https://github.com/NVIDIA-Merlin/Transformers4Rec/blob/main/merlin_standard_lib/schema/tag.py

https://github.com/NVIDIA-Merlin/Transformers4Rec/blob/main/examples/tutorial/schema_tutorial.pb

https://github.com/NVIDIA-Merlin/core/blob/main/merlin/schema/tags.py

https://github.com/NVIDIA-Merlin/core/blob/main/tests/unit/schema/test_column_schemas.py

## Create schema proto manullay

[[QST] How/Where Is the Schema Generated? #271](https://github.com/NVIDIA-Merlin/Transformers4Rec/issues/271#issuecomment-934850026)

(on Oct 6, 2021)
> The latest version of the NVTabular library (used for the ETL pipeline) automatically outputs a schema file in the protobuf text format (schema.pbtxt) together with the parquet files of processed data. This is still a work in progress and we'll include the necessary support in the future release of Transformers4Rec.

## Universal external-data wrapper for NVTabular

https://github.com/NVIDIA-Merlin/core/blob/main/merlin/io/dataset.py

## TrainingArguments

Transformers4Rec inherits huggingface transformers library. You can adjust TrainingArguments.

https://huggingface.co/docs/transformers/v4.25.1/en/main_classes/trainer#transformers.TrainingArguments
