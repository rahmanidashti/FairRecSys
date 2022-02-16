# FairRecSys

<img src="./images/banner.jpeg" alt="Markdown Monster icon" style="float: left; margin-right: 10px;" />

## Model

## Datasets
We add all of the datasets into the <a href="./datasets">`datasets`</a> folder with the user and item groups. Each folder in `datasets` folder is relevant to one dataset and each of which contains a folder called `groups`. The `groups` folder includes to subfolders, `items` and `users`. The  `items` folder contains short-head and long-tail item groups while the  `users` folder includes user group files based on two user grouping methods (i.e., 5% and 20%).

## How to Run?

<a href="https://colab.research.google.com/github/rahmanidashti/FairRecSys/blob/main/UFR.ipynb">Run model</a>

## Results
Due to space limitations we add the results on the `Epinions` and `Last.fm` datasets into the paper. However, we add the final results of all datasets into the <a href="./tables">`tables`</a> folder accroding to each user grouping method (i.e., interactions and popular consumption). There, we have two folders, `5` and `20`, for user grouping based on interactions (5) and popular consumption (20).

## Team
<a href=#>Hossein A. Rahmani</a>, Wen Intelligence Group, UCL

<a href=#>Mohammadmehdi Naghiaei</a>, University of Southern California

<a href=#>Mahdi Dehghan</a>, SBU, Shahid Beheshti University

<a href=#>Mohammad Aliannejadi</a>, IRLab, University of Amsterdam

## Citation
If you use our source code, dataset, and experiments for your research or development, please cite the following paper:

```
@inproceedings{rahmani2022fairrecsys,
  title={Experiments on Generalizability of User-Oriented Fairness in Recommender Systems},
  author={Hossein A. Rahmani, Mohammadmehdi Naghiaei, Mahdi Dehghan, Mohammad Aliannejadi},
  booktitle={SIGIR},
  year={2022}
}
```

## Acknowledgements

## Todo
[] Adding the datasets charactristics in the daataset readme