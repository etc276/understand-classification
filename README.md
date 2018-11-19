# understand-classification

## Step 1: Design a set of rules to classify data

### problem description
* problem: decide which color I like
* data size: 200
* feature:
    * R - red
    * G - green
    * B - blue
    * range from 0 to 255

### absolutely right rule
* rule 0: 60 < R < 155 and G < 100 and B > 160 ===> yes

### cross validation

* training: 60%
* testing: 40%

## Step 2: Use the data generated in Step 1 to construct the classification model

* decision tree
    * Accuracy: 97%

* visulization
![](https://i.imgur.com/1vei3ft.png)

## Step 3: Compare the rules in the decision tree from Step 2 and the rules used to generate the "absolutely right" data

## Absolutely right rule
* rule 0: 60 < R < 155 and G < 100 and B > 160 ===> yes


## Result from decision tree
* rule 1: R ≤ 54 and G ≤ 118.5 and B ≤ 164.5 ===> no
* rule 2: B ≤ 160.5 ===> no

## Compare
* rule 1: similar to absolutely right rule
* rule 2: far from absolutely right rule
* result: only 97% accuracy
* guess: feature overlapping in label 0 (as you see in rule 2)

## Step 4: Discuss anything you can
> try other classifiers
>

* Random Forest: higher accuracy than decision tree
* Extra Tree: lower accuracy than decicsion tree