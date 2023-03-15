# Code

The code contains:

* **Models folders**: 3 folders that contain the Domain component for each domain in the benchmark domain

* **Dictionaries folder**: a folder that contains the dictionaries. For each domain we have:
    * Action dictionary: a dictionary that enumerates all the considered actions for a given domain
    * Goal dictionary: a dictionary that enumerates all the considered goals (facts) for a given domain

* **goal_rec.yml**: a YML file that contains all the python libraries required to run out python notebook

```sh
conda env create -f goal_rec.yml
```

* **GRNet_approach.ipynb**: a python notebook that contains the running code for our approach

You can download some test instances by cloning this publicly avaliable goal recognition dataset:
https://github.com/pucrs-automated-planning/goal-plan-recognition-dataset or use the provided test sets in the **testsets** folder.

```sh
git clone https://github.com/pucrs-automated-planning/goal-plan-recognition-dataset
```

Put the models in a folder named ```models``` in the same directory as the notebook.

In order to run the notebook: 

```sh
cd code
jupyter lab
```

And select the notebook in the GUI.

From section **1.4 GRNet execution** customize the parameters to fit your tests 

```python
domain=C.DOMAIN_NAME
domain_dir='path_to_the_problems/'
```

Please note that `domain_dir` should contain three folders called `30`, `50` and `70` which contain the archive goal recognition files with the corresponding observability percentage.