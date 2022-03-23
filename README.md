
#  Personality Prediction from Text
## Description
- Data on personality types was gathered (MBTI and big five) for further information, see below.
- The situation on the data was evaluated. There is much more MBTI data available which is scientifically less reliant, but there is only very few data on the BIG FIVE traits. Machine Learning algorithms thrive on data so a approach created to combine MBTI and BIG Five data. 
- The data from three different sources was converted in mutual form and preprocessed to the needs of ML algorithms
- features from text were extracted to vectorize the data with bags of words and GloVe approach
- several supervised classification learning algorithm were used and trained to predict on future unknown text
- the results of the classifiers were evaluated
- a predictor was developed who predicts traits and visualizes them:

![Image](https://github.com/joegog/personality-detection-text/blob/master/docu/predict.PNG?raw=true)
## The big five personality model
The Big Five personality traits, also known as the five-factor model (FFM) and the OCEAN model, is a taxonomy, or grouping, for personality traits.
The five factors are:
- Openness to experience (inventive/curious vs. consistent/cautious)
- Conscientiousness (efficient/organized vs. easy-going/careless)
- Extraversion (outgoing/energetic vs. solitary/reserved)
- Agreeableness (friendly/compassionate vs. challenging/detached)
- Neuroticism (sensitive/nervous vs. secure/confident)

## The Myers–Briggs Type Indicator 
The Myers–Briggs Type Indicator (MBTI) is an introspective self-report questionnaire indicating differing psychological preferences in how people perceive the world and make decisions. 

| _             | Subjective                | Objective                           |
| ------------- |:-------------:            | --------------------------------:   |
| Deductive     | **I**ntuition/**S**ensing |  **I**ntroversion/**E**xtraversion	|
| Inductive     | **F**eeling/Thinking      |   **P**erception/**J**udging        |

The combinations as four pairs of preferences lead to 16 possible combinations aka types. The 16 types are typically referred to by an abbreviation of four letters—the initial letters of each of their four type preferences (except in the case of intuition, which uses the abbreviation "N" to distinguish it from introversion). For instance:

ESTJ: extraversion (E), sensing (S), thinking (T), judgment (J)
INFP: introversion (I), intuition (N), feeling (F), perception (P)	              	

## Differences and commonalities of the Big Five and MBTI

Adrian Furnham 1996 concludes a corellation of his 1996 paper [The big five versus the big four: the relationship between the Myers-Briggs Type Indicator (MBTI) and NEO-PI five factor model of personality](https://www.sciencedirect.com/science/article/abs/pii/0191886996000335) concludes a correlation between these traits from:

|  MBTI            |  Big Five                           |
| :-------------:            | --------------------------------:   |
| **I**ntuition/**S**ensing |  Openness to experience (corellates with N)   |
|  **F**eeling/Thinking      |   Agreeableness (correlates with F)       |
|  **P**erception/**J**udging      |   Conscientiousness (correlates with J)        |
|  **I**ntroversion/**E**xtraversion      |   Extraversion (correlates with E)       |
|  not available in MBTI              |   Neuroticism       |

## Goal of this project
- Predicting personality traits in high accuracy with classifiers trained from text data which is labeled with the personality types.
- gathering familiarty with machine learning core concepts
- trying to find an approach to combine MBTI data with BIG FIVE data to increase amount of data to train machine learning classifiers

### Results

| EXT | NEU| AGR | CON | OPN|
| :-------------:| :--------:   |  :--------:   |  :--------:   | :--------:   |
|   77.18    | 61.74|  75.51  | 70.34 | 80.39 |

## Dataset used
### Personality Type Dataset "mbti_1.csv"
From [Kaggle](https://www.kaggle.com/datasnaek/mbti-type): This data was collected through the [PersonalityCafe forum(https://www.personalitycafe.com/forum/), as it provides a large selection of people and their MBTI personality type, as well as what they have written.

## Used Methods
### Classification
- SVM (sklearn)
- Decision Tree (sklearn)
- Naive Bayes (sklearn)
- Logistic Regression (sklearn)
- Random Forest (sklearn)

# repo overview / how to use

## if you just want to run pretrained models
just open predict.ipynb and use your own text on the variable "text" if you want, check analysis_results.ipynb - this compares the feature extractions and classifiers in their score
