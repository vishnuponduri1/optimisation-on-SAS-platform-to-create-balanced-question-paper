# optimisation-on-SAS-platform-to-create-balanced-question-paper
# Question Paper Optimization Project

## I. Problem Context
The objective of this project is to assist a professor in creating two sets of 50-question papers from a bank of 154 questions—one for the final exam and one for practice. The challenge is to adhere to specific constraints provided by the professor.

## II. Parameters and Sets
We have defined a "Question" set with indices for attributes like "Frenemy," "topic," "objective," and “force.” The "Objective" parameter is indexed by "objective." The "Frenemy groups" set is utilized to extract corresponding frenemy data from the Question Bank. Additionally, three parameters—"Correct," "Objective Questions," indexed by "Question" and "objective," respectively—are populated with dataset information. The set "Exams" includes elements "Practice" and "Live."

## III. Decision Variables
A total of 308 variables are introduced to generate two sets of question papers. These variables, with values of 0 or 1 (0 indicating exclusion and 1 indicating inclusion), are named "SelQnsLive,i" and "SelQnsPractice,j" where "i" and "j" are indices representing questions.

## IV. Constraints
Several constraints are applied to meet the professor's requirements. Constraints include limiting the number of questions in each set, adhering to objective question limits, and managing questions related to frenemy groups. Additionally, forced question inclusion and constraints related to overlapping questions between sets are implemented.

## V. Objective
The goal is to minimize the difference in easiness between the two question paper sets while considering historical correctness percentages. The linearized objective function ensures a balance in difficulty.

## VI. Linearization
To make the problem solvable, the objective and constraint related to overlap are linearized. Surplus and difference variables are introduced in the objective function, and binary variables are defined for the overlap constraint.

## VII. Assumptions
Assumptions include equating historically low correctness with higher question difficulty and assuming similarity in pedagogy, curriculum, and materials for the upcoming exam-takers.

## VIII. Output
The output includes solver analysis and sensitivity analysis. The professor now has the capability to create well-balanced question papers with important objectives. The solution can be seamlessly integrated into downstream applications for automated computerized exams in the future by adjusting constraints as needed.
