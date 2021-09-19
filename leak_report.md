# Leak report

The memory leak in clean_whitespace.c happens when the when using the variable
cleaned in the is_cleaned function by setting it equal to the strip version of the string. The variable is then used to compare
whether the str and cleaned version are the same or different but is not freed in the is_cleaned function. This leads to a memory leak. This
memory leak can be fixed by using free(cleaned) before the function ends or return statement. An if statement should also be implemented to check if the strlen(cleaned)
is not equal to 0.
