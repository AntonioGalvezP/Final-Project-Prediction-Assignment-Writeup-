---
title: "Final Project_Prediction Assignment Writeup"
author: "Antonio Gálvez"
date: "3/12/2019"
output: html_document
---

## Getting and cleaning data

The information regarding to models developed in this document are available in the follow website: http://groupware.les.inf.puc-rio.br/har
On the another hand, both sets of data used as a training data and test data are available from the links below:
 - Training data
https://d396qusza40orc.cloudfront.net/predmachlearn/pml-training.csv
 - Test data
https://d396qusza40orc.cloudfront.net/predmachlearn/pml-testing.csv

The first following lines download the data from the links shown above.
And the last lines load the data cleaned into the memory.

```{r ECHO = FALSE}
url_train <- "https://d396qusza40orc.cloudfront.net/predmachlearn/pml-training.csv"
url_testin <- "https://d396qusza40orc.cloudfront.net/predmachlearn/pml-testing.csv"

download.file(url_train, file.path(getwd(), "pml-training.csv"))
download.file(url_testin, file.path(getwd(), "pml-testing.csv"))


training1 = read.csv("pml-training.csv", na.strings = c("NA", "#DIV/0!" , ""))
testing1 = read.csv("pml-testing.csv", na.strings = c("NA", "#DIV/0!" , ""))

training12 <- training1[,colSums(is.na(training1)) == 0]
testing12 <- testing1[,colSums(is.na(testing1)) == 0]
training1 <- training12[,-c(1:7)]
testing1 <- testing12[,-c(1:7)]
dim(training1); dim(testing1)
```

## Partitioning the training dataset

These few lines of code make the partition of the training data set into two datasets. The new trainig dataset contains a 70% of the data, and the rest is in saved unto the new testing dataset. 

```{r}
set.seed(1991)
inTrain <- caret::createDataPartition(y = training1$classe, p = 0.7, list = FALSE)
training <- training1[inTrain, ]
testing <- training1[-inTrain, ]
dim(training); dim(testing)
```

## Plotting the classe
The following line plots the classe paramenter using the new dataset defined for training.
```{r}
plot(training$classe, col = "orange", main="Bar Plot of the partitioning by Classe parameter", xlab="classe variable", ylab="Frequency")

```
## Prediction model: Decision tree
First model and its prediction.
```{r}
Modelo1 <- rpart::rpart(classe ~ ., data= training, method="class")
pred_Mod1 <- predict(Modelo1, testing, type = "class")

rpart.plot::rpart.plot(Modelo1, main="Decision Tree", extra="auto", faclen=0)
```
```{r}
caret::confusionMatrix(pred_Mod1, testing$classe)
```
## Prediction model: Random Forest Algorithm
Second model and its prediction.
```{r}
Modelo2 <- randomForest::randomForest(classe ~., training, method = "class")
pred_Mod2 <- predict(Modelo2, testing, type = "class")

caret::confusionMatrix(pred_Mod2, testing$classe)
```
##  Comparison and decision

Random Forest algorithm achieve better results than Decision Trees.
Accuracy for Random Forest model was 1.000 (95% CI: (0.994, 1)) compared to Accuracy : 0.9997 (95% CI : (0.9988, 1) for Decision Tree model. 
For the reason mentioned abobe the random Forest model is choosen.

## Submission
The following line makes a prediction using the Random Forest Model defined above and the dataset given in the problem description.
```{r}
predict(Modelo2, testing1, type = "class")
```
