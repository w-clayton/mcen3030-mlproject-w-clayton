# mcen3030-mlproject-w-clayton

# Initial Prompt:

I would like to do a machine learning project where the goal is to predict whether a coffee bean is one of a specific class based on a data set of physical measurements of beans with known classes. I have a spreadsheet with columns ‘area’, ‘perimeter’, ‘MajorAxisLenght’, ‘MinorAxisLength’, 'Aspect Ratio', 'Eccentricity', 'ConvexArea', 'EquivDiameter', 'Extent', 'Solidity', 'Roundness', 'Compactness', 'ShapeFactor1', 'ShapeFactor2', 'ShapeFactor3', 'ShapeFactor4', and ‘Class’. There are approximately 13612 rows. I will ask for matlab code soon, but first: Can we talk about the best way to model this data set?


# LLM Response 1


I used Chatgpt as the LLM to prompt for this project. After my first prompt it sugested using a Random Forest model. It suggested this model because it can handle multiple parameters (like the various physical measurements of the beans) well to find a classification for a new input, it doesn't require complicated tuning once it has the reference data, it can determine which parameters are most important for classification, and it has built in validation based on "out-of-bag" error.

# Confusion Matrix From Code_1

<img width="898" height="519" alt="Screenshot 2026-04-17 at 11 34 01 PM" src="https://github.com/user-attachments/assets/f99ea685-d2f1-4eac-8ca7-6fedf97812cf" />

The confusion matrix shows how the Random Forest Model uses predictions to classify the beans. Most predictions are along the primary diagonal, which means that the model is fairly accurate. Bombay beans were classified perfectly, while Sira beans were mis-classified the most.


# Code Iteration Prompts

After talking with the LLM, the second iteration of the code has a larger number of trees so the model has more accuracy when assigning a class to a bean. It also increased the number of splits from each tree to make the model recognize more detailed patterns when making a classification, and increased the number of features per split so there is a better chance of finding the optimal classification from each tree in the model.


# Feature Importance Plot From Code_2



<img width="568" height="433" alt="Screenshot 2026-04-18 at 12 02 58 AM" src="https://github.com/user-attachments/assets/6e7e2fa6-7cdc-4df4-81a7-b6bccbb32a0a" />


This plot gives each measured parameter of the beans a rating for how important they are to assign a coff,ee bean to a class. The most important parameters are Roundness, Compactness, Shape Factor 3, and the axis lenghts. While extent is barely considered.





