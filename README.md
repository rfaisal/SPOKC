###********************NOTE********************
This Project is currently being contributed as part of Research Interface (RIN).

RIN Project page: http://www.rin-bd.org/serial-parallel-opt-c/

RIN Project page on Github: http://rfaisal.github.io/SPOKC/project-rin.html

RIN Contributors: Sabbir Ahmad and Rakin Haider

RIN Project Progress: https://www.pivotaltracker.com/s/projects/827507
###***********************************************

# SPOKC


The Serial-Parallel Optimization Kit in C (SPOKC) consists of implementations of different optimization algorithms. The project was started to bring the optimization algorithms under a flexible standard, so that any researcher developing new optimization algorithms can use this kit for comparisns without having to reimplement again. Every algorithm in this kit has a serial and a parallel implementation. The parallel implemetations uses the OpenMP model. 

## Class of optimization algorithms

SPOKC supports a wide range of optimization algorithms. The SPOKC standard algorithms minimizes (you have to reformulate for maximization problems) a function `f:R^n->R`, given a set of constraints. Since there are already very efficient libearies for linear optimization algorithms, SPOCK mainly targets algorithms for solving non-linear, discontinuous, weird optimization problems.


## SPOKC Standard

1. An SPOKC Standard algorithm is a minimization algorithm.
2. The decision variables (`x`) are of dimension `n`, represented by `double x[n]` in the algorithm. Both `x` and `n` are reserved keywords for the SPOKC Standard.
3. The objective function `f:R^n->R` is represened by `double f(double x[])` in the code. `f` is a reserved keyword for the SPOKC Standard.
4. The problem can have `m` constraints. `m` is a reserved keyword for the SPOKC Standard.
5. The name of the algorithm starts with either s (for serial) or p (for parallel) followed by the full name of the algorithm with the words seperated by underscoves. For example, `void p_nelder_mead_simplex(double (*f)(double[]), void (*constrain)(double[],int n), ...)` represents a parallel implementation of the Nelder Mead Simplex algorithm.

Test sets for unit testing, extensive performance testing, and 100% code coverage will be provided.

This is open source, so feel free to contribute.
