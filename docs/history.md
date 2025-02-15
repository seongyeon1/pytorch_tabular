# History

## 1.0.1 (2023-01-20)

- Bugfix for default metric for binary classification




## 1.0.0 (2023-01-18)

- Added a new task - Self Supervised Learning (SSL) and a separate training API for it.
- Added new SOTA model - Gated Additive Tree Ensembles (GATE).
- Added one SSL model - Denoising AutoEncoder.
- Added lots of new tutorials and updated entire documentation.
- Improved code documentation and type hints.
- Separated a Model into separate Embedding, Backbone, and Head.
- Refactored all models to separate Backbone as native PyTorch Model(nn.Module).
- Refactored commonly used modules (layers, activations etc. to a common module).
- Changed MixedDensityNetworks completely (breaking change). Now MDN is a head you can use with any model.
- Enabled a low level api for training model.
- Enabled saving and loading of datamodule.
- Added trainer_kwargs to pass any trainer argument PyTorch Lightning supports.
- Added Early Stopping and Model Checkpoint kwargs to use all the arguments in PyTorch Lightining.
- Enabled prediction using GPUs in predict method.
- Added `reset_model` to reset model weights to random.
- Added many save and load functions including ONNX(experimental).
- Added random seed as a parameter.
- Switched over completely to Rich progressbars from tqdm.
- Fixed class-balancing / mu propagation and set default to 1.0.
- Added PyTorch Profiler for debugging performance issues.
- Fixed bugs with FTTransformer and TabTransformer.
- Updated MixedDensityNetworks fixing a bug with lambda_pi.
- Many CI/CD improvements including complete integration with GitHub Actions.
- Upgraded all dependencies, including PyTorch Lightning, pandas, to latest versions and added dependabot to manage it going forward.
- Added pre-commit to ensure code integrity and standardization.

## 0.7.0 (2021-09-01)

- Implemented TabTransformer and FTTransformer models
- Included capability to save a model using GPU an load in CPU
- Made the temp folder pytorch tabular specific to avoid conflicts with other tmp folders.
- Some bug fixes
- Edited an error out of Advanced Tutorial in docs

## 0.6.0 (2021-06-21)

- Upgraded versions of PyTorch Lightning to 1.3.6
- Changed the way `gpus` parameter is handled to avoid confusion. `None` is CPU, `-1` is all GPUs, `int` is number of GPUs
- Added a few more Trainer Params like `deterministic`, `auto_select_gpus`
- Some bug fixes and changes to docs
- Added `seed_everything` to the fit method to ensure reproducibility
- Refactored data_aware_initialization to be part of the BaseModel. Inherited Models can override the method to implement data aware initialization techniques

## 0.5.0 (2021-03-18)

- Added more documentation
- Added Zenodo citation

## 0.4.0 (2021-03-18)

- Added AutoInt Model
- Added Mixture Density Networks
- Refactored the classes to separate backbones from the head of the models
- Changed the saving and loading model to work for custom parameters that you pass in `fit`

## 0.3.0 (2021-03-02)

- Fixed a bug on inference

## 0.2.0 (2021-02-07)

- Fixed an issue with torch.clip and torch version
- Fixed an issue with `gpus` parameter in TrainerConfig, by setting default value to `None` for CPU
- Added feature to use custom sampler in the training dataloader
- Updated documentation and added a new tutorial for imbalanced classification

## 0.0.1 (2021-01-26)

- First release on PyPI.
