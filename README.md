# IntrusionDetection
![image](https://user-images.githubusercontent.com/109751694/209487319-4c020afe-7292-4f94-bd77-5e6a85f4c49e.png)

## DataSet 
KISTI+IDS2021-CDMC
Description:[153830 records] divided into two parts: a training set [123040 records] and testing set [30790 records]. For the training set contains three features (category, word_vector, label), and for the testing set consists of two features (category, word_vector). For category feature presents the level of the attack, word_vector feature presents the payload words in 100 dimensions for each word, and label feature presents two labels (Malicious [1], benign [2]) with balanced number for each one. There are no null records in the dataset.

## Methodology
Our proposed approach methodology involves following steps: 
	Preprocessing, Feature Engineering, Feature selection.
Using the feature word vector that represents the payload words in 100 dimensions for each word in the payload. We convert the huge number of word vector into only one vector, so instead of representing every payload on more than a vector we decided to apply mean and represent the whole payload with the mean vector and as shown in the figure before applying the mean on the data was not well distributed and after applying the mean vector and feed our Deep Learning models with the new extracted feature.
The experimental results show that the IDS’ design using this approach has a high accuracy with low false positives and false negatives for new and modified attacks.

All models used the same hyperparameters which are, the optimizer was set to Adam with Learning rate = 0.001 and early stopping that monitor the model loss. We applied 5-fold cross validation on all the models.

![image](https://user-images.githubusercontent.com/109751694/209487870-e250fccf-b44a-4dba-97c3-06c8e9772ae9.png)

![image](https://user-images.githubusercontent.com/109751694/209487891-d114c362-5fd4-480a-823a-e3863c6f6419.png)

![image](https://user-images.githubusercontent.com/109751694/209487911-729fcd46-30c8-48c8-904c-8311a157ddc4.png)

![image](https://user-images.githubusercontent.com/109751694/209487943-66d207b3-dcb5-42a0-b775-e19909eeb92e.png)

## Experiment 1 
![image](https://user-images.githubusercontent.com/109751694/209487958-b4f8e802-c7e0-4639-ab5c-a23c94a4d195.png)
## Experiment 2 
![image](https://user-images.githubusercontent.com/109751694/209487982-1d346e88-9559-4d80-85e4-1298dc01a2d1.png)
## Experiment 3
![image](https://user-images.githubusercontent.com/109751694/209487993-5426c609-8c01-4062-898d-5e30a2050452.png)
## Experiment 4
![image](https://user-images.githubusercontent.com/109751694/209487997-a6b4997e-a55e-47fe-9356-1f68b09f4447.png)

## All Results
![image](https://user-images.githubusercontent.com/109751694/209488040-6df8d4f3-4773-431c-bed9-3c84d98f1446.png)

## Final Model 
![image](https://user-images.githubusercontent.com/109751694/209488058-fcc776ef-e11f-435e-ac8d-ecb8039dd009.png)

## Error Analysis 
![image](https://user-images.githubusercontent.com/109751694/209488089-a7f46615-bcac-4483-a4f8-c41003aa70bd.png)

The bad results from the extracted features could be a result cause we have many samples in attacks and benign class so its high overlapping case were the chance for that sample Is equally the same.
