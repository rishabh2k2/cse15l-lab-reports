# **Lab 3**

Author: *Rishabh Kalyanakumar*  
- The first command that we are going over with find  
  this command print lines which have the word in between '' and the type -f searches the files and prints it out 


#  
   **Example 1**   
   - In this example the command finds the word "share" in the Media directory and prints it out           
    
    rishabhk@RiSHABHK Media % find ./ -type f -name "*.txt" -exec grep 'shared'  {} \;
    
    quilting business on the loan application, shared $15,600 in
    was caught with cocaine three blocks from the apartment she shared
    staff attorney shared an office with a colleague. But confidential
    Christenson, pointed out that the shared facility will also be
    information about the latest salary increase or layoffs is shared

# 
  **Example 2**  
  - In this example the command finds the word "Transmit" in the About_LSC sub-directory and prints it out  
    
        rishabhk@RiSHABHK About_LSC % find ./ -type f -name "*.txt" -exec grep 'transmit'  {} \; 
   
        transmit information pertaining to its own program, Rosenberger v.
        and faster and more efficient transmittal of information to
        I am pleased to transmit the comments of the Legal Services
        which the government "used private speakers to transmit
        not itself speak or subsidize transmittal of a message it favors
#
 **Example 3**  
 - In this example the command finds the word "Death" in the biomeddirectory and prints it out  
           
           rishabhk@RiSHABHK biomed % find ./ -type f -name "*.txt" -exec grep 'Death'  {} \;   
          
          Case-Fatality Rates and Causes of Death
          Causes of Death and 2-Year Case-Fatality
          intracellular redox state [ 60 ] . Death induced by TNFα is
          nick end labeling (TUNEL) (In situ Cell Death Detection
          determined using the Cell Death Detection ELISA Kit assay
          and control subclones failed to grow. Death after
          (Boehringer - In Situ Cell Death Detection Kit,
          with the Cell Death ELISA (DNA fragmentation assay).

#  
 - The next Command finds files that were modified using -mtime
 - In example 1 we can see that the command prints out the files that were modified in the last 3 days in the 911report directory  

 **Example 1**  
 
    
    rishabhk@RiSHABHK 911report % find . -mtime -3
     .
     ./chapter-13.4.txt
     ./chapter-13.5.txt
     ./chapter-13.1.txt
     ./chapter-13.2.txt
     ./chapter-13.3.txt
     ./chapter-3.txt
     ./chapter-2.txt
     ./chapter-1.txt
     ./chapter-5.txt
     ./chapter-6.txt
     ./chapter-7.txt
     ./chapter-9.txt
     ./chapter-8.txt
     ./preface.txt
     ./chapter-12.txt
     ./chapter-10.txt
     ./chapter-11.txt

-  In example 2 we can see that the command prints out the files that were modified in the last 3 days in the Alcohol_Problems sub-directory  

**Example 2**
#
     rishabhk@RiSHABHK Alcohol_Problems % find . -mtime -3    
    .
    ./Session2-PDF.txt
    ./Session3-PDF.txt
    ./DraftRecom-PDF.txt
    ./Session4-PDF.txt

-  In example 3 we can see that the command prints out the files that were modified in the last 3 days in the Post_Rate_Comm sub-directory  

**Example 3**
#
    rishabhk@RiSHABHK Post_Rate_Comm % find . -mtime -3 
    .
    ./Gleiman_EMASpeech.txt
    ./Mitchell_spyros-first-class.txt
    ./Cohenetal_CreamSkimming.txt
    ./Cohenetal_DeliveryCost.txt
    ./Mitchell_RMVancouver.txt
    ./Gleiman_gca2000.txt
    ./Cohenetal_Cost_Function.txt  
    ./Redacted_Study.txt
    ./Mitchell_6-17-Mit.txt
    ./Cohenetal_comparison.txt
    ./Cohenetal_Scale.txt
    ./Cohenetal_RuralDelivery.txt
    ./ReportToCongress2002WEB.txt
    ./WolakSpeech_usps.txt

- the next command finds the size of of whatever is specified
#
**Example 1**  

- In Example 1 we find the directories of the specified size in this case it is between 3 and 10k
     
       rishabhk@RiSHABHK technical % find . -type d -size +3k  -size -5k
       ./government/Media

**Example 2**  

- In example we the files in the techinal directory that are of 2048 bytes or less
#     
      rishabhk@RiSHABHK technical % find . -type f -size -2048c  
      ./government/Media/Helping_Hands.txt
      ./government/Media/Campaign_Pays.txt
      ./government/Media/Fire_Victims_Sue.txt
      ./government/Media/Court_Keeps_Judge_From.txt
      ./government/Media/It_Pays_to_Know.txt
      ./government/Media/Self-Help_Website.txt
      ./government/Media/Justice_requests.txt
      ./government/Media/Wilmington_lawyer.txt
     ./government/Media/Lawyer_Web_Survey.txt
     ./plos/pmed.0020048.txt
     ./plos/pmed.0020028.txt
     ./plos/pmed.0020191.txt
     ./plos/pmed.0020226.txt
     ./plos/pmed.0020192.txt
     ./plos/pmed.0020157.txt
     ./plos/pmed.0020082.txt
     ./plos/pmed.0020120.txt
     ./plos/hellodoc.txt
