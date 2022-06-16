
# Applying StereoSet to CoLAKE

## Reproducing Results
To reproduce our results for the bias in each model:

1. Run `make` from the `code` folder. This step evaluates the biases on each model.
2. Run the scoring script with respect to each model: `python3 evaluation.py --gold-file ../data/dev.json --predictions-dir predictions/`. 

We have provided our predictions in the `predictions/` folder, and the output of the evaluation script in `predictions.txt`. We have also included code to replicate our numbers on each table in the `tables/` folder. Please feel free to file an issue if anything is off; we strongly believe in reproducible research and extensible codebases.

## Citation
To cite StereoSet: 

```
@misc{nadeem2020stereoset,
    title={StereoSet: Measuring stereotypical bias in pretrained language models},
    author={Moin Nadeem and Anna Bethke and Siva Reddy},
    year={2020},
    eprint={2004.09456},
    archivePrefix={arXiv},
    primaryClass={cs.CL}
}
```
