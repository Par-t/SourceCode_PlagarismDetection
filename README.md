# Source Code Plagiarism Detection

This project focuses on detecting plagiarism in source code using machine learning techniques. 

[Model1.ipynb] utilises only 3 basic features to compare code files to train our classification mode. Basic NLP techniques have been used to give our first initial and basic model with 77% accuracy using DecisionTreeClassifier.

[Model2.ipynb] utilizes the `javalang` library to traverse through the abstract syntax tree (AST) of Java code and extract relevant features for training a classification model. The goal is to identify similarities and differences between code snippets to determine if there is any potential plagiarism. This improved model gave an accuracy of upto 89%.

The following features are extracted from the code snippets:

- Similarity in variable and method names using edit distance and Levenshtein distance
- Difference in the number of variables, lines of code, loops, and control structures
- Cosine similarity in method return types and variable data types

A class has been defined with methods that analyze one code at a time to store details about that program. These details are then compared between pairs of code snippets, forming the training and testing dataset.

The dataset used for training and evaluation can be found at [Source Code Plagiarism Dataset](https://github.com/oscarkarnalim/sourcecodeplagiarismdataset). It consists of 7 original code files, 105 non-plagiarized files, and 355 plagiarized files. Each original file has a corresponding set of non-plagiarized and plagiarized files. Each case represents either an original-plagiarized code pair or an original-non-plagiarized code pair.

Multiple classification models have been evaluated, and the highest accuracy was achieved using the RandomForestClassifier.

## Credits

- [javalang](https://github.com/c2nes/javalang): A library for parsing Java code and extracting AST information.
- [Source Code Plagiarism Dataset](https://github.com/oscarkarnalim/sourcecodeplagiarismdataset): A dataset containing original, non-plagiarized, and plagiarized code files for training and evaluation purposes.

