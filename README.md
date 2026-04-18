# mcen3030-mlproject-w-clayton

# Initial Prompt:

I would like to do a machine learning project where the goal is to predict whether a coffee bean is one of a specific class based on a data set of physical measurements of beans with known classes. I have a spreadsheet with columns ‘area’, ‘perimeter’, ‘MajorAxisLenght’, ‘MinorAxisLength’, 'Aspect Ratio', 'Eccentricity', 'ConvexArea', 'EquivDiameter', 'Extent', 'Solidity', 'Roundness', 'Compactness', 'ShapeFactor1', 'ShapeFactor2', 'ShapeFactor3', 'ShapeFactor4', and ‘Class’. There are approximately 13612 rows. I will ask for matlab code soon, but first: Can we talk about the best way to model this data set?


# LLM Response 1


I used Chatgpt as the LLM to prompt for this project. After my first prompt it sugested using a Random Forest model. It suggested this model because it can handle multiple parameters (like the various physical measurements of the beans) well to find a classification for a new input, it doesn't require complicated tuning once it has the reference data, it can determine which parameters are most important for classification, and it has built in validation based on "out-of-bag" error
