We use the cancer transcriptomes from The Cancer Genome Atlas PanCancerAtlas project to interrogate gene expression states induced by deleterious mutations and copy number alterations and predict the type of cancer for a given expression
Performed Dimensionality Reduction on the data by converting set of possibly correlated genetical features into linearly uncorrelated variables using PCA and t-SNE
Used Random Forest Classifier and Support Vector Machines for prediction with a 99.17% cross-validation accuracy after hyper-parameter tuning

The data set is a part of RNA-Seq (HiSeq) PANCAN data set, which is a random extraction of gene expressions of patients having different types of tumor, namely Breast invasive carcinoma (BRCA), Kidney renal clear cell carcinoma (KIRC), Colon adenocarcinoma (COAD), Lung adenocarcinoma (LUAD) and Prostate adenocarcinoma (PRAD). This data set is created by University of Genoa and redistributed under creative commons license. 

Data Transformation: 

Encoded labels with value between 0 and n_classes-1. Using the LabelEncoder() function we have transformed the labels from ['BRCA', 'COAD', 'KIRC', 'LUAD', 'PRAD'] to [0, 1, 2, 3, 4], for the purposes of convenient numerical computations. The labels of the data set are separately provided and requires explicit merging.  

Data Normalization: 

Feature scaling through standardization (or Z-score normalization) can be an important preprocessing step for many machine learning algorithms. Standardization involves rescaling the features such that they have the properties of a standard normal distribution with a mean of zero and a standard deviation of 1. 

In our project, the data has been normalized using the StandardScaler() function. Standardized features by removing the mean and scaling to unit variance. The standard score of a sample x is calculated as: z = (x - u) / s     

Model Selection 

We have used the following models: 

Naïve Bayes
Gaussian NB 
Bernoulli NB 
Decision Trees 
SVM (Support Vector Machines) 
Random Forest 

Metrics and Performance Evaluation: 

The train accuracies, test accuracies (using cross validation) of all the classifiers was computed using our training/validation data. F1 score is used to evaluate the projects after model selection, since it is sensitive to both precision and recall. 



