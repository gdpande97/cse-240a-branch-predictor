# The Branch Predictor Project

## Welcome to the project

This is going to be the first programming assignment in CSE240A. The theme is, as the title suggests, a branch predictor. As I'm sure you know from what is covered in class, Branch Predictors are a critical part of the processor's front end, providing a great performance boost to the overall performance of the processor. In this assignment, we aren't giving you a full fledged processor simulator, but a rather simple model of a branch predictor. This model will have a few functions which you will have to add to, and design 2 new predictors in code. As a skeleton framework, we have provided you with an existing implementation of the GShare Predictor (correlating predictor). 

## The Task
For this task, you will build 2 predictors based on the skeleton code. The first will be a Tournament branch predictor based on the Alpha 21264 processor. The other will be a custom implementation of your own choice which needs to outperform both the GShare and the Tournament predictors. This will also be a competition between the class itself, to get the maximum possible performance from your processor. The reward for the top 6 performers is extra credit points. The other condition in this scenario, is that you have only 32KB of hardware budget, so make sure that your data structures fit within this budget. 

Here are some papers that you can refer to for the custom design:

### [TAGE](https://www.irisa.fr/caps/people/seznec/JILP-COTTAGE.pdf)
### [Perceptron](https://www.cs.utexas.edu/~lin/papers/hpca01.pdf)
### [YAGS](https://safari.ethz.ch/digitaltechnik/spring2021/lib/exe/fetch.php?media=mudge_yags.pdf)

You can of course search on your own and implement any other branch predictor you want. 

## Academic Integrity

This assignment is to be done individually by every student. Please make sure you do not copy a single line of code from any source. Not from other students, not from the web, not from anywhere. We have very sophisticated tools to discover if you did. This is a graduate class and we have the very highest expectations for integrity. You should expect that if you do so, even in very small amounts, you will be caught, you will be asked to leave the program, and if an international student, required to leave the country.

## Get Started

Download the code using the following link on github : `https://github.com/gdpande97/240a-branch-predictor.git`
Once you have checked out this repository, start adding your code into this. To compile, run the following command from within the `src` directory: `make all` or `make`. This will compile your code and generate output files. You will also get a executable binary called `predictor`. To run this, you need to give the following command:
bunzip2 -kc /path/to/trace | ./predictor --predictor_type

You will add the tournament code based on the implementation that can be found in the Alpha 21264 paper. There is a slight modification to the paper design - we are using 2 bit saturating counters for the predictor instead of 3.

## What should you edit?

You need to edit the predictor.c for the most part. Add your functions and make sure they are referenced correctly so that your code runs perfectly. Do not edit any other files.

## Deliverables

The code, of course!!! We need to get the link of a git repository that you are using to store this code. Please make sure you are using the main branch of the git repository for your final submission. Along with this, you will also submit a PDF, which will include a brief description of your choice of custom predictor and its implementation. You should also include a table which shows the performance of the tournament predictor as well as your custom predictor for all the given traces. You should also include a table which shows your total hardware budget usage.



