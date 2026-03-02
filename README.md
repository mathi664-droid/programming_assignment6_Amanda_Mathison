# programming_assignment6_Amanda_Mathison

Problem Statement: For this assignment we are tasked with modifying ls.c and whoami.c. We are modifying ls.c so that we are able to run ls like ls -1 where it will display file permissions, file size, owner, file name, modified date, etc. For part two of this assignment we are tasked with modifting whoam.c so that it will print "You Are: ___" instead of just the user name.

Describe the Solution: I changed line 2266 (format = (0 <= format_opt ? format_opt : ls_mode == LS_LS ? long_format //changed it to : ls_mode == LS_MULTI_COL ? many_per_line : /* ls_mode == LS_LONG_FORMAT */ long_format);). I changed this line so that when no options are given, it will give the long_format instead. For whoami.c the original program just printed the username(puts(pw->pw_name);). I changed it to printf("You are: %s\n", pw->pw_name); so now it will print "You are: username".

Pros: 
-Small changes to the code 
-Doesn't change any other outcomes of the code 

Cons:
-It was hard trying to focus on changing the format because there's a lot of code to look through, but when you know what you're looking for, it becomes a lot easier.
-Not windows friendly
-If Coreutils is updated or changed, it might affect the outcome of the code
