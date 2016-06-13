Codeforces Parser Python  v1.5.1
=================

Summary
-------

[Codeforces](http://codeforces.com/) is a website for _competitive programming_. It holds contests, so-called **Codeforces Rounds**, about every week.

This is a python program that parses the sample tests from the contest problem pages. For each problem, it generates the sample input/output files and a shell script to run sample tests.

This project is adapted from the C++ Codeforces Parser you can find in this article: [http://codeforces.com/blog/entry/10416](http://codeforces.com/blog/entry/10416), the major difference being right now that Python scripts are generated, instead of C++.

### Example:
`./parse.py contest_number (e.g. ./parse.py 513)`

Where `512` is the contest number, not the round number! Check the URL of the contest on your browser, that is the number you are supposed to use.

### Effect:

##### What will happen, for example, if `./parse.py 512` is executed?

1. Directories `512/A`, `512/B`, `512/C`, `512/D` and so on are created depending on the contest number of problems.
2. For each problem, `main.py` is copied and renamed to the problem letter to the corresponding directory. **You can put the path of your usual template in `parse.py:20`**.
3. Problem page is downloaded from Codeforces website, and parsed. Sample input/output files are generated, e.g. `input1`, `output1`, `input2`, `output2` and so on. You can create your own test cases after that, just keep the same naming format as others test cases.
4. A script `test.sh` is generated. You can use it to compile and run the sample tests after you finish coding. Just run `./test.sh` in the problem directory.

##### What will happen if `./test.sh` is executed?

1. Run each sample tests on your Python program, and check the output by `diff`. If it's correct, print **Accepted**, or else print the sample test that went wrong.
2. Please note that for problems with multiple correct answers it might say that your output is incorrect.

### Collaborators and Versions:

##### List of Collaborators of the C++ version:
+ [johnathan79717](http://codeforces.com/profile/johnathan79717)
+ [brunoja](http://codeforces.com/profile/brunoja)
+ [Matthias Kauer (mini addition)]

