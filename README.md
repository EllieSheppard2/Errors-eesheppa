# Errors
This project is riddled with errors. Please fix all the bugs!

## Setup
Use this Guided Project template to create a new repository (see [GitHub-with-CLion](https://github.com/uvmcs2300f2025/GitHub-with-CLion) repo for directions).
**Your repository must be named with the convention: Errors-netid**, where netid is your UVM NetID username.

When you first put it into CLion, the Build and Run buttons will be grayed out and unclickable. This is intentional. You will need to start fixing bugs before these buttons can be used.

Remember to commit and push frequently.

## Errors
There are three types of errors:
1. **Compiler errors** prevent your program from running. These are typically CMake or syntax errors.
1. **Runtime errors** occur while the program is running and prevent an exit code of zero. Examples of this include a non-zero exit code and an infinite loop.
1. **Logic errors** are when your program runs to completion (with exit code zero) but does not behave the way you intended. The best way to catch logic errors is through extensive testing and/or the use of the debugger.

For this project, you have been given a very broken program and it is your job to fix it. For each error you fix, log it in the table below.

## Logging Errors
Every time you fix a bug, log it in the README file here:

| Type of error (compiler, runtime, logic) | File           | Description                                                                         | Fix                                                                   |
|------------------------------------------|----------------|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Example: compiler                        | CMakeLists.txt | "project PROJECT called with incorrect number of arguments"                         | Added the project name to line 2                                      |
| compiler                                 | spie.cpp       | constructor syntax SPIE_Game() {                                                    | prefixed constructor                                                  |
| compiler                                 | main.cpp       | incorrect construction of game                                                      | added/removed parentheses                                             |
| logic                                    | main.cpp       | missing break in switch statement                                                   | added break statment, moved some code onto seperate lines for clarity | 
| compiler                                 | main.cpp       | missing brace in if (score==0){ ...                                                 | added closing brace                                                   |
| compiler                                 | spie.h         | missing std::                                                                       | added std:: in front of vecotr, ostream, instream                     |
| compiler                                 | spie.cpp       | missing return statement in get player choice                                       | added return choice                                                   |
| compiler                                 | main.cpp       | missing {} around switch / case blocks                                              | added {} around switch / case blocks                                  |
| compiler                                 | main.cpp       | missing ; on return statement at end of file                                        | added ; to return                                                     |
| runtime                                  | spie.cpp       | index does not adjust when element is erased                                        | we only go forward if element is not erased                           |
| compiler                                 | main.cpp       | including wrong file type                                                           | changed include spie.cpp to spie.h                                    ||                                          |                |                                                                              |                                                                        |
| logic                                    | spie.cpp       | while choice != s ... does not evaluate to "while choice is not s, p, i or e        | changed to using "choice != && choice!="                              |                                                                       |
| logic                                    | spie.cpp       | add_winning_numbers never actually adds a number, so it doesnt display when playing | added "winning_numbers.push_back(new_number);"                        |
| logic                                    | spie.cpp       | when rolling for example 6 if a winning number is 6, scramble does not replace      | changed around logic, w is no longer declared twice                   |
| logic                                    | spie.cpp       | rolling does not give a valid range for two die (0-10 not 2-12)                     | added + 1 to return (rand() % 6)                                      |






### Grading Rubric
- [ ] (2 pts) Fix at least one CMake compiler error (not including the one already given).
- [ ] (3 pts) Fix at least one other compiler error.
- [ ] (3 pts) Fix at least one runtime error.
- [ ] (3 pts) Fix at least one logic error.
- [ ] (5 pts) The README table is populated fully and correctly.
- [ ] (4 pts) Fix at least 15 errors total (note: errors you create do not count).
