Inferential Statistics Test
Instructions
This test contains 25 questions on inferential statistics (ANOVA, t-tests, chi-square tests, z-tests). Each question uses a Kaggle dataset (Iris, Titanic, or Student Performance). Datasets can be downloaded from:

Iris: https://www.kaggle.com/datasets/uciml/iris Titanic: https://www.kaggle.com/datasets/c/h/titanic Student Performance: https://www.kaggle.com/datasets/spscientist/students-performance-in-exams

Fill in the Python code to perform the specified statistical test and interpret the results (alpha = 0.05). Use pandas, numpy, scipy.stats, and statsmodels for calculations. Each question is worth 4 points (Total: 100 points). import pandas as pd import numpy as np from scipy import stats import statsmodels.api as sm from statsmodels.formula.api import ols import warnings warnings.filterwarnings('ignore')

Question 1: One-sample t-test on Iris dataset Task: Load the Iris dataset and test if the mean sepal length of Iris-setosa is equal to 5.0. iris = pd.read_csv('iris.csv') setosa_sepal_length = iris[iris['Species'] == 'Iris-setosa']['SepalLengthCm']

Fill in: Perform one-sample t-test
Q1: Is the mean sepal length significantly different from 5.0? (Answer: p < 0.05, so yes/no) Question 2: Two-sample t-test on Iris dataset Task: Compare sepal width of Iris-setosa and Iris-versicolor. setosa_sepal_width = iris[iris['Species'] == 'Iris-setosa']['SepalWidthCm'] versicolor_sepal_width = iris[iris['Species'] == 'Iris-versicolor']['SepalWidthCm']

Fill in: Perform two-sample t-test (assume equal variances)
Q2: Are the means significantly different? (Answer: p < 0.05, so yes/no) Question 3: One-way ANOVA on Iris dataset Task: Test if petal length differs across all three Iris species.

Fill in: Perform one-way ANOVA
Q3: Is there a significant difference in petal length across species? (Answer: p < 0.05, so yes/no) Question 4: Chi-square test on Titanic dataset Task: Load the Titanic dataset and test if survival is independent of passenger class (Pclass). titanic = pd.read_csv('titanic.csv') contingency_table = pd.crosstab(titanic['Survived'], titanic['Pclass'])

Fill in: Perform chi-square test
Q4: Is survival independent of passenger class? (Answer: p < 0.05, so yes/no) Question 5: One-sample z-test on Titanic dataset Task: Test if the mean age of passengers is equal to 30 (assume population std = 14.5).

Fill in: Perform one-sample z-test
Q5: Is the mean age significantly different from 30? (Answer: p < 0.05, so yes/no) Question 6: Independent t-test on Titanic dataset Task: Compare mean age of male vs. female passengers. male_age = titanic[titanic['Sex'] == 'male']['Age'].dropna() female_age = titanic[titanic['Sex'] == 'female']['Age'].dropna()

Fill in: Perform independent t-test
Q6: Are the mean ages significantly different? (Answer: p < 0.05, so yes/no) Question 7: One-way ANOVA on Titanic dataset Task: Test if fare differs across passenger classes (Pclass).

Fill in: Perform one-way ANOVA
Q7: Is there a significant difference in fare across classes? (Answer: p < 0.05, so yes/no) Question 8: Chi-square test on Titanic dataset Task: Test if survival is independent of sex. contingency_table = pd.crosstab(titanic['Survived'], titanic['Sex'])

Fill in: Perform chi-square test
Q8: Is survival independent of sex? (Answer: p < 0.05, so yes/no) Question 9: Paired t-test on Student Performance dataset Task: Load the Student Performance dataset and test if math score and reading score differ for the same students. students = pd.read_csv('StudentsPerformance.csv')

Fill in: Perform paired t-test
Q9: Are math and reading scores significantly different? (Answer: p < 0.05, so yes/no) Question 10: One-sample z-test on Student Performance dataset Task: Test if the mean writing score is equal to 70 (assume population std = 15).

Fill in: Perform one-sample z-test
Q10: Is the mean writing score significantly different from 70? (Answer: p < 0.05, so yes/no) Question 11: Two-sample t-test on Student Performance dataset Task: Compare math scores of male vs. female students. male_math = students[students['gender'] == 'male']['math score'] female_math = students[students['gender'] == 'female']['math score']

Fill in: Perform two-sample t-test
Q11: Are math scores significantly different between genders? (Answer: p < 0.05, so yes/no) Question 12: One-way ANOVA on Student Performance dataset Task: Test if math scores differ across ethnic groups (race/ethnicity).

Fill in: Perform one-way ANOVA
Q12: Is there a significant difference in math scores across ethnic groups? (Answer: p < 0.05, so yes/no) Question 13: Chi-square test on Student Performance dataset Task: Test if gender is independent of test preparation course completion. contingency_table = pd.crosstab(students['gender'], students['test preparation course'])

Fill in: Perform chi-square test
Q13: Is gender independent of test preparation? (Answer: p < 0.05, so yes/no) Question 14: One-sample t-test on Iris dataset Task: Test if the mean petal width of Iris-virginica is equal to 2.0. virginica_petal_width = iris[iris['Species'] == 'Iris-virginica']['PetalWidthCm']

Fill in: Perform one-sample t-test
Q14: Is the mean petal width significantly different from 2.0? (Answer: p < 0.05, so yes/no) Question 15: Two-sample t-test on Titanic dataset Task: Compare fare paid by survivors vs. non-survivors. survivor_fare = titanic[titanic['Survived'] == 1]['Fare'].dropna() nonsurvivor_fare = titanic[titanic['Survived'] == 0]['Fare'].dropna()

Fill in: Perform two-sample t-test (assume unequal variances)
Q15: Are fares significantly different between survivors and non-survivors? (Answer: p < 0.05, so yes/no) Question 16: One-way ANOVA on Iris dataset Task: Test if sepal length differs across Iris species.

Fill in: Perform one-way ANOVA
Q16: Is there a significant difference in sepal length across species? (Answer: p < 0.05, so yes/no) Question 17: Chi-square test on Titanic dataset Task: Test if embarkation port (Embarked) is independent of passenger class. contingency_table = pd.crosstab(titanic['Embarked'], titanic['Pclass'])

Fill in: Perform chi-square test
Q17: Is embarkation port independent of passenger class? (Answer: p < 0.05, so yes/no) Question 18: One-sample z-test on Student Performance dataset Task: Test if the mean math score is equal to 65 (assume population std = 15).

Fill in: Perform one-sample z-test
Q18: Is the mean math score significantly different from 65? (Answer: p < 0.05, so yes/no) Question 19: Paired t-test on Student Performance dataset Task: Test if reading score and writing score differ for the same students.

Fill in: Perform paired t-test
Q19: Are reading and writing scores significantly different? (Answer: p < 0.05, so yes/no) Question 20: Two-sample t-test on Iris dataset Task: Compare petal length of Iris-versicolor and Iris-virginica. versicolor_petal_length = iris[iris['Species'] == 'Iris-versicolor']['PetalLengthCm'] virginica_petal_length = iris[iris['Species'] == 'Iris-virginica']['PetalLengthCm']

Fill in: Perform two-sample t-test
Q20: Are petal lengths significantly different? (Answer: p < 0.05, so yes/no) Question 21: One-way ANOVA on Student Performance dataset Task: Test if reading scores differ across test preparation course status.

Fill in: Perform one-way ANOVA
Q21: Is there a significant difference in reading scores by test preparation? (Answer: p < 0.05, so yes/no) Question 22: Chi-square test on Student Performance dataset Task: Test if parental level of education is independent of test preparation course. contingency_table = pd.crosstab(students['parental level of education'], students['test preparation course'])

Fill in: Perform chi-square test
Q22: Is parental education independent of test preparation? (Answer: p < 0.05, so yes/no) Question 23: One-sample t-test on Titanic dataset Task: Test if the mean fare is equal to 30.

Fill in: Perform one-sample t-test
Q23: Is the mean fare significantly different from 30? (Answer: p < 0.05, so yes/no) Question 24: Two-sample t-test on Student Performance dataset Task: Compare writing scores of students with vs. without test preparation. prep_writing = students[students['test preparation course'] == 'completed']['writing score'] noprep_writing = students[students['test preparation course'] == 'none']['writing score']

Fill in: Perform two-sample t-test
Q24: Are writing scores significantly different by test preparation? (Answer: p < 0.05, so yes/no) Question 25: One-way ANOVA on Titanic dataset Task: Test if age differs across embarkation ports (Embarked).

Fill in: Perform one-way ANOVA
Q25: Is there a significant difference in age across embarkation ports? (Answer: p < 0.05, so yes/no) End of Test To complete:

Fill in the missing code for all questions. For each question, perform the specified statistical test and interpret the p-value to determine significance (alpha = 0.05). Submit your completed code and answers to the significance questions.# inferential_statistics
