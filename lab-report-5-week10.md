# Lab 5 Report
# Part 1

Code block of grade.sh:

# 
   

     set -e
     rm -rf student-submission
     mkdir student-submission

     git clone $1 student submission

     cp TestListExamples.java student-submission
     cd student-submission

     CPATH=.:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar

     if [[ -f ListExamples.java ]];
     then
       echo "FILE FOUND (1/1)"
     else
        echo "FILE NOT FOUND (0/1)"
        echo "SCORE: 0/5"
        exit 1
     fi

     set +e

     javac -cp $CPATH *.java > compile-err.txt

     if [[ $? -eq 0 ]]
     then
      echo "COMPILED SUCCESFFULLY (1/1)"
     else
       echo "COMPILED UNSUCCESSFULLY (0/1)"
       echo "SCORE: 1/5"
       cat compile-err.txt
        exit 2
     fi

      java -cp $CPATH org.junit.runner.JUnitCore TestListExamples > test-err.txt

     if [[ $? -eq 0 ]]
     then 
      echo "ALL TESTS PASSED"
      echo "SCORE: 5/5"
      exit
      else
      echo "TEST FAILED"
      echo "SCORE: 2/5"
      cat test-err.txt
     exit 3
        

I was having trouble running the GradeServer.java file (I ended up running it locally) as you can you see below: 
![image](Server.png)


# Example 1
- Repository Link: https://github.com/ucsd-cse15l-f22/list-methods-corrected
#
    rishabhk@RiSHABHK cse15l-lab-reports % bash grade.sh  https://github.com/ucsd-cse15l-f22/list-methods-corrected
    Cloning into 'student-submission'...
    remote: Enumerating objects: 3, done.
    remote: Counting objects: 100% (3/3), done.
    remote: Compressing objects: 100% (2/2), done.
    remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
    Receiving objects: 100% (3/3), done.
    FILE FOUND(1/1)
    COMPILED SUCCESSFULy (1/1)
    ALL TESTS PASSED
    SCORE: 5/5

# Example 2
  I ran into errors when working on example 2
- Repository Link: https://github.com/ucsd-cse15l-f22/list-methods-lab3
 # 
     Cloning into 'student-submission'...
     remote: Enumerating objects: 3, done.
     remote: Counting objects: 100% (3/3), done.
     remote: Compressing objects: 100% (2/2), done.
     remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
     Receiving objects: 100% (3/3), done.
     cp: TestListExamples.java: No such file or directory
     cp: lib/hamcrest-core-1.3.jar: No such file or directory
     cp: lib/junit-4.13.2.jar: No such file or directory
     FILE FOUND
     error: no source files
     COMPILED UNSUCCESFFULLY (0/1) 
     SCORE: 1/5

# Example 3 
- Repository Link: https://github.com/ucsd-cse15l-f22/list-methods-compile-error
# 
     Cloning into 'student-submission'...
     remote: Enumerating objects: 3, done.
     remote: Counting objects: 100% (3/3), done.
     remote: Compressing objects: 100% (2/2), done.
     remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
     Receiving objects: 100% (3/3), done.
     FILE FOUND(1/1)
     ListExamples.java:15: error: ';' expected
              result.add(0,s)
                             ^
     1 error    
     COMPILED UNSUCCESSFULY (0/1)
     SCORE: 1/5

# Part 2 
# Script Trace:

# 
    set -e
    rm -rf student-submission
    mkdir student-submission

    git clone $1 student submission

    cp TestListExamples.java student-submission
    cd student-submission

    CPATH=.:../lib/hamcrest-core-1.3.jar:../lib/junit-4.13.2.jar


- ```set -e``` is used to exits the code in the case that there is error it automatically exit the code
- This script removes the "student-submission" and creates a new directory and the git repository is cloned and the TestListExamples and is moved into the new directory

- ```CPATH``` is used to store the jUnit command

#

     if [[ -f ListExamples.java ]];
     then
       echo "FILE FOUND (1/1)"
     else
       echo "FILE NOT FOUND (0/1)"
       echo "SCORE: 0/5"
       exit 1
     fi

     set +e
    

- We can use the ```-f``` command allows the Script script to search if the ```ListExamples.java``` file exists,  if the file exists the student gets 1 point if not the student does not recieve a point and the script is exited when the exit code is used

- The ```set+e``` command is present so the script will not immediatley exit when an exit code it used

# 
  
     javac -cp $CPATH *.java > compile-err.txt

      if [[ $? -eq 0 ]]
      then
         echo "COMPILED SUCCESFFULLY (1/1)"
      else
         echo "COMPILED UNSUCCESSFULLY (0/1)"
         echo "SCORE: 1/5"
         cat compile-err.txt
         exit 2
      fi

-  The ``` javac``` command compiles all the files in the folder and the stderr is redirected to ```compile-err.txt```

- The if-statement will compare the exit code of the compiling if it is 0. if the exit code is 0 the student gets 1 point for compiling, if not the student does not recieve points and the stderr is written to compile-err.txt to show the student the error message.

#

     java -cp $CPATH org.junit.runner.JUnitCore TestListExamples > test-err.txt

     if [[ $? -eq 0 ]]
     then 
       echo "ALL TESTS PASSED"
       echo "SCORE: 5/5"
       exit
     else
       echo "TEST FAILED"
       echo "SCORE: 2/5"
       cat test-err.txt
       exit 3
     fi

- The if statement compares the exit code of java to see if it is equal to 0 
- if the exit code is 0, the student recieves max points for passing every test.
- if not the student does not recieve point and the stderr is written and the students can see what errror is causing them to loose points 
