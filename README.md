# Human-Activity-Recognition-using-mobile-phones-by-Boosting-and-Stacking

![boosting](https://user-images.githubusercontent.com/81983943/145528014-90970c18-f062-4a69-bd9f-c89336675158.png)

# Ensemble Methods-

Ensemble methods are commonly used to boost predictive accuracy by combining the predictions of multiple machine learning models. The traditional approach has been to combine so-called “weak” learners. However, the latest approach is to create an ensemble of a well-chosen collection of strong yet diverse models.

# Voting-Classifier:

Voting is the easiest way of aggregating/combining predictions from different machine learning algorithms. Voting Classifier is not an actual classifier but it uses a majority vote (Hard Vote)or the average predicted probabilities (soft vote) to predict the class labels. Such a classifier can be useful for a set of equally well performing model in order to balance out their individual weaknesses.

There are two types of voting options we can use in the voting classifier.

# Hard Voting(majority/popularity voting):
In Hard voting we take predicted class labels from all the models and the class that receives the highest number of votes will be chosen as the predicted Class. It is a simplest case of majority voting.

Lets take an example of 3 binary classifiers to predict the class 0 or 1.

Classifier 1- predicts class 1

Classifier 2- predicts class 0

Classifier 3- predicts class 0

Predicted class (Y^)=mode{1,0,0}=0

Since two out of three classifiers predicted ‘0’, class ‘0’ will be the final ensemble decision.

# Soft Voting:
In soft voting we predict the class labels based on the predicted probabilities p for each classifier. Lets assume the probabilities from the previous classifiers are as below.

Classifier 1- [0.9,0.1]

Classifier 2- [0.8,0.2]

Classifier 3- [0.4,0.6]

We compute the average probabilities for each class.

p(0)=(0.9+0.8+0.4)/3=0.7

p(1)=(0.1+0.2+0.6)/3=0.3

Since the probability of class 0 is the highest which is 0.7, our final class will be ‘0’ based on the soft voting. Soft voting gives the better accuracy as it considers the actual probability of each class from the model output.

# In Dataset-
we have to predict human activity using mobile phones that he is sleeping, lying, sitting, standing, walking etc based on the some features.

target variable's classes-----> ['LAYING', 'SITTING', 'STANDING', 'WALKING', 'WALKING_DOWNSTAIRS', 'WALKING_UPSTAIRS']
