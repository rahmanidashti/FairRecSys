# FairRecSys

<img src="./images/banner.jpeg" alt="Markdown Monster icon" style="float: left; margin-right: 10px;" />

## Model

## Datasets
We add all of the datasets into the <a href="./datasets">`datasets`</a> folder with the user and item groups. Each folder in `datasets` folder is relevant to one dataset and each of which contains a folder called `groups`. The `groups` folder includes to subfolders, `items` and `users`. The  `items` folder contains short-head and long-tail item groups while the  `users` folder includes user group files based on two user grouping methods (i.e., 5% and 20%).

## How to Run?

### Datasets: `grouping.ipnb`

### Model: `UFR.ipynb`
In order to make easy to use the reproducibility of URF mode, we create a notebook which can be run on Google Colab easily. Thus, you only need to config the dataset and then run the cells and get the final reuslts in CSV files. To do this, the follwing steps need to be taken:

- First, you can open the notebook of URF model using <a href="https://colab.research.google.com/github/rahmanidashti/FairRecSys/blob/main/UFR.ipynb" target="_blank">Run model</a> or copy and pate the follwing link in your browser:

    ```
    https://colab.research.google.com/github/rahmanidashti/FairRecSys/blob/main/UFR.ipynb
    ```

- Next, you can config the dataset using the follwoing cell in the notebook:

    ```
    # dataset congfig
    ds_names = ["AmazonOffice"]
    is_implicit = False
    ds_users = ['2']
    ds_items = ['020']
    ```

    where `ds_names` is the name of the dataset, `is_implicit` indicate the feedback type, `ds_users` refer to the user grouing methods (`005 -> interactions` and `2 -> popular consumption`), and `ds_items` indicate the item grouping method which is `020`, indicating short-head and long-tail items grpouing according to top 20% popular items. You can check all the datasets, their attributes, users and items grouping in <a href="./datasets">`dataset`</a> folder.

- Finally, when you run the model the reuslts for each recommendation algorithms will be stored in a CSV file called `results_DATASET_MODEL.csv` including the follwing columns:

    ```
    Dataset: Name of the dataset
    Model: Name of base recommendation algorithm
    GUser: User group
    GItem: Item group
    Type: Fairness type which is either N (i.e, fairness-unaware) or C (i.e., user fairness-aware)
    User_EPS: User epsilon
    Item_EPS: -
    ndcg_ALL: NDCG for all users
    ndcg_ACT: NDCG for advaneteged/active users
    ndcg_INACT: NDCG for disadvaneteged/inactive users
    Pre_ALL: Precision for all all users
    Pre_ACT: Precision for advaneteged/active users
    Pre_INACT: Precision for disadvaneteged/inactive users
    Rec_ALL: Recall for all users
    Rec_ACT: Recall for advaneteged/active users
    Rec_INACT: Recall for disadvaneteged/inactive users
    Nov_ALL: Novelty for all users
    Nov_ACT: Novelty for advaneteged/active users
    Nov_INACT: Novelty for disadvaneteged/inactive users
    Cov_ALL: Coverage for all users
    Cov_ACT: Coverage for advaneteged/active users
    Cov_INACT: Coverage for disadvaneteged/inactive users
    Active_GAP: GAP for all advaneteged/active users
    Inactive_Gap: GAP for all disadvaneteged/inactive users
    Short_Items: The numebr of short-head recommended items
    Long_Items: The numebr of long-tail recommended items
    All_Items: The numebr of all recommended items
    ```

### Analysis and Plots: `analysis.ipynb`

## Tables (Results on Paper)
Due to space limitations we add the results on the `Epinions` and `Last.fm` datasets into the paper. However, we add the final results of all datasets into the <a href="./tables">`tables`</a> folder accroding to each user grouping method (i.e., interactions and popular consumption). There, we have two folders, `005` and `2`, for user grouping based on interactions (005) and popular consumption (2).

## Team
<a href="http://rahmanidashti.github.io/">Hossein A. Rahmani</a>, Wen Intelligence Group, UCL

<a href=#>Mohammadmehdi Naghiaei</a>, University of Southern California

<a href="http://dehghanm.github.io/">Mahdi Dehghan</a>, SBU, Shahid Beheshti University

<a href="http://aliannejadi.com/">Mohammad Aliannejadi</a>, IRLab, University of Amsterdam

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
TBA

## Contact
If you have any questions, do not hesitate to contact us by `h.rahmani@ucl.ac.uk` or `rahmanidashti@gmail.com`, we will be happy to assist.

## Todo
- [X] Adding the datasets charactristics in the daataset readme
- [X] Adding description on how to run the model
- [X] Adding raw results files
