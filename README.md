# Schrödinger’s Bat: Diffusion Models Sometimes Generate Polysemous Words in Superposition

## Paper

This repository contains code accompanying ['Schrödinger’s Bat: Diffusion Models Sometimes Generate Polysemous Words in Superposition'](link) by Jennifer C. White and Ryan Cotterell (pre-print).

## Instructions

Download [SCAN](https://github.com/brendenlake/SCAN) and place it in the directory.

Running `python train.py --best_hyperparams SPLIT_NAME` will train a model on the given split using our best-performing hyperparameters for that split.

SCAN Splits available are `simple`, `add_jump`, `length_generalization` and `around_right`.

Custom hyperparameters can also be passed in as arguments. Run `python train.py -h` to see information on these arguments.

Following training, the model with lowest loss on the dev set will be evaluated on the test set and saved with a name in the format `{test_accuracy}___{scan_split}__{K}__{num_filters}__{hidden_size}__{embed_dim}__{batch_size}__{learning_rate}.model`.

Running `python test.py --model_path /path/to/model --scan_split SPLIT_NAME` will evaluate a model on the test set of the given split.

## Citation

```
@inproceedings{white-cotterell-2022-equivariant,
    title = "Equivariant Transduction Through Invariant Alignment",
    author = "White, Jennifer C.  and
      Cotterell, Ryan",
    booktitle = "Proceedings of the 29th International Conference on 
Computational Linguistics",
    month = oct,
    year = "2022",
    publisher = "International Committee on Computational Linguistics",
}
```
