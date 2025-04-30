# Devtools Part 2
1. The bug was that the function was handling the num1 and num2 as strings and then concatenating the values as a string.
    - E.g. 1 + 2 = "12" because "1" + "2" = "12"
2. I fixed the bug by casting both num1 and num2 as number so number arithmetic can be performed on them.