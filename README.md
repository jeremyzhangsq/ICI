# ICI Reproducibility

## Diffusion models benchmarking

### Requirements

* python2.7 or python3.7
* sklearn, pandas, networkx, numpy

### Datasets
* path: `ICI/datasets/`
* sources for raw data: [Digg](https://www.isi.edu/~lerman/downloads/digg2009.html), [Twitter](https://snap.stanford.edu/data/higgs-twitter.html).
* data preprocessing scripts: `clean_diggs.py;clean_twitter.py`
* preprocessed datasets: `[filename].edgelist;[filename].seed;[filename].spread`

### Model implementations
* path: `ICI/utils/`

### Run

* command:
```
python benchmark.py [--model model_name] [--dataset file_name] [--output 0/1] [--repeat simulation_times] [--step spread_in_each_step] [--beta ICI_param] [--gamma ICI_param];
```
* example:
```
python benchmark.py --model ici --dataset digg --output 1 --repeat 1000 --step 10 --beta 0.9 --gamma 0.6;
```
* Input arguments

  - datasets: `--dataset={"digg","twitter"}`
  - support models: `--model={"ic", "icm", "icn", "icr", "lt", "ftm", "ltc"}`
  - output mode: print all results by `--output 1`
  
### Citation
Please kindly cite our work if you find our paper or codes helpful.
``` 
@inproceedings{zhang2024information,
  title={Information Diffusion Meets Invitation Mechanism},
  author={Zhang, Shiqi and Sun, Jiachen and Lin, Wenqing and Xiao, Xiaokui and Huang, Yiqian and Tang, Bo},
  booktitle={Companion Proceedings of the ACM on Web Conference 2024},
  pages={383--392},
  year={2024}
}
```

 
