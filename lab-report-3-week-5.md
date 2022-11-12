# **Lab 3**

Author: *Rishabh Kalyanakumar*  
# Command Line Option #1:  ```grep-c```  

- The grep-c command allows the user to easily search for keywords or phrase in multiple files and it prints out the files where they are found in.  

# Example 1

    rishabhk@RiSHABHK technical % cd 911report
    rishabhk@RiSHABHK 911report % grep -c "President" chapter-6.txt
    71

- In this Example, I used the ``grep-c`` command to find out how many times the word president is mentioned in the champter-6.txt file. This command is very useful to determine the repetion of waords in a text file or code.
  


 # **Example 2**  
    
        
        rishabhk@RiSHABHK 911report % grep -c "first" *.txt    
        chapter-1.txt:43chapter-1.txt:0                                                                                                         
        chapter-10.txt:0                                                                                                        
        chapter-11.txt:0                                                                                                        
        chapter-12.txt:0                                                                                                        
        chapter-13.1.txt:0                                                                                                      
        chapter-13.2.txt:0                                                                                                      
        chapter-13.3.txt:0                                                                                                      
        chapter-13.4.txt:0                                                                                                      
        chapter-13.5.txt:0                                                                                                      
        chapter-2.txt:0                                                                                                         
        chapter-3.txt:0                                                                                                         
        chapter-5.txt:0                                                                                                         
        chapter-6.txt:0                                                                                                         
        chapter-7.txt:0                                                                                                         
        chapter-8.txt:0                                                                                                         
        chapter-9.txt:0                                                                                         
        preface.txt:1
        
  - In this example I used the ```Preface``` keyword in order to find the text file with the preface in book/novel. this is very useful as it can help users find a certain chapter or sub division instead of manually looking through the files.
#
#  **Example 3**  
           
        
           rishabhk@RiSHABHK 911report % cd ..
           rishabhk@RiSHABHK technical % ls 
           911report       biomed          government      plos
           rishabhk@RiSHABHK technical % cd plos
           rishabhk@RiSHABHK plos % grep -c "brains" journal.pbio.* 
           journal.pbio.0020001.txt:0
           journal.pbio.0020010.txt:0
           journal.pbio.0020012.txt:0
           journal.pbio.0020013.txt:0
           journal.pbio.0020019.txt:0
           journal.pbio.0020028.txt:0
           journal.pbio.0020035.txt:0
           journal.pbio.0020040.txt:0
           journal.pbio.0020042.txt:0
           journal.pbio.0020043.txt:0
           journal.pbio.0020046.txt:0
           journal.pbio.0020047.txt:2
           journal.pbio.0020052.txt:0
           journal.pbio.0020053.txt:0
           journal.pbio.0020054.txt:0
           journal.pbio.0020063.txt:0
           journal.pbio.0020064.txt:0
           journal.pbio.0020067.txt:0
           journal.pbio.0020068.txt:0
           journal.pbio.0020071.txt:0
           journal.pbio.0020073.txt:0
           journal.pbio.0020100.txt:0
           journal.pbio.0020101.txt:0
           journal.pbio.0020105.txt:0
           journal.pbio.0020112.txt:0
           journal.pbio.0020113.txt:0
           journal.pbio.0020116.txt:0
           journal.pbio.0020121.txt:1
           journal.pbio.0020125.txt:0
           journal.pbio.0020127.txt:0
           journal.pbio.0020133.txt:0
           journal.pbio.0020140.txt:0
           journal.pbio.0020145.txt:0
           journal.pbio.0020146.txt:0
           journal.pbio.0020147.txt:0
           journal.pbio.0020148.txt:0
           journal.pbio.0020150.txt:3
           journal.pbio.0020156.txt:0
           journal.pbio.0020161.txt:1
           journal.pbio.0020164.txt:0
           journal.pbio.0020169.txt:0
           journal.pbio.0020172.txt:0
           journal.pbio.0020183.txt:0
           journal.pbio.0020187.txt:0
           journal.pbio.0020190.txt:0
           journal.pbio.0020206.txt:0
           journal.pbio.0020213.txt:0
           journal.pbio.0020214.txt:0
           journal.pbio.0020215.txt:0
           journal.pbio.0020216.txt:1
           journal.pbio.0020223.txt:0
           journal.pbio.0020224.txt:0
           journal.pbio.0020228.txt:0
           journal.pbio.0020232.txt:0
           journal.pbio.0020241.txt:0
           journal.pbio.0020262.txt:0
           journal.pbio.0020263.txt:0
           journal.pbio.0020267.txt:11
           journal.pbio.0020272.txt:1
           journal.pbio.0020276.txt:0
           journal.pbio.0020297.txt:0
           journal.pbio.0020302.txt:0
           journal.pbio.0020306.txt:1
           journal.pbio.0020307.txt:0
           journal.pbio.0020310.txt:0
           journal.pbio.0020311.txt:0
           journal.pbio.0020337.txt:0
           journal.pbio.0020346.txt:1
           journal.pbio.0020347.txt:0
           journal.pbio.0020348.txt:0
           journal.pbio.0020350.txt:0
           journal.pbio.0020353.txt:0
           journal.pbio.0020354.txt:0
           journal.pbio.0020394.txt:2
           journal.pbio.0020400.txt:0
           journal.pbio.0020401.txt:1
           journal.pbio.0020404.txt:0
           journal.pbio.0020406.txt:0
           journal.pbio.0020419.txt:0
           journal.pbio.0020420.txt:0
           journal.pbio.0020430.txt:0
           journal.pbio.0020431.txt:0
           journal.pbio.0020439.txt:0
           journal.pbio.0020440.txt:0
           journal.pbio.0030021.txt:0
           journal.pbio.0030024.txt:0
           journal.pbio.0030032.txt:0
           journal.pbio.0030050.txt:24
           journal.pbio.0030051.txt:0
           journal.pbio.0030056.txt:0
           journal.pbio.0030062.txt:0
           journal.pbio.0030065.txt:0
           journal.pbio.0030076.txt:0
           journal.pbio.0030094.txt:0
           journal.pbio.0030097.txt:0
           journal.pbio.0030102.txt:0
           journal.pbio.0030105.txt:0
           journal.pbio.0030127.txt:0
           journal.pbio.0030129.txt:0
           journal.pbio.0030131.txt:0
           journal.pbio.0030136.txt:0
           journal.pbio.0030137.txt:1  

 - In this example I wanted to find out which text files in ```journal.pbio``` files were oriented towards topic of the human brain. In this case it can be determined that ```journal.pbio.0030050.txt``` was oriented toward the topic of the brain because it mentioned "brain" 24 times in the text file. 
 #       
# **Command Line Option #2:**  ```grep-w```  
 - The ```grep-w``` allows the user to print out all the sentances contaning a keyword as an argument for the command  

 # Example 1  
 
    
    
    rishabhk@RiSHABHK 911report % grep -w president chapter-6.txt  
    His one-day stopover on March 25, 2000, was the first time a U.S. president had been
    Similarly, Berger recalled that to go to war, a president needs to be able to say
    not think it would be responsible for a president to launch an invasion of another president in 2001.
    the margins, eliciting written responses. The new president, by contrast, reinstated
    After nine years on the NSC staff and more than three years as the president's
    

-  In This example i used ```grep-w``` to print out every single line that had the word president in the champter 6 text file. This is useful for those who need to skim through content and gain a general understanding

 # Example 2

     rishabhk@RiSHABHK Alcohol_Problems % find . -mtime -3    
    . PREFACE
    We present the narrative of this report and the recommendations that flow from it tothe President of the United States, the United States Congress, and the Americanpeople for their consideration. Ten Commissioners-five Republicans and five Democrats chosen by elected leaders from our nation's capital at a time of great
    partisan division-have come together to present this report without dissent. We have come together with a unity of purpose because our nation demands it.September 11, 2001, was a day of unprecedented shock and suffering in the history of
    the United States. The nation was unprepared. How did this happen, and how can weavoid such tragedy again? To answer these questions, the Congress and the President created the National Commission on Terrorist Attacks Upon the United States (Public Law 107-306, November 27, 2002). Our mandate was sweeping. The law directed us to investigate "facts and circumstances relating to the terrorist attacks of September 11, 2001," including those relating to intelligence agencies, law enforcement agencies, diplomacy, immigration issues and border control, the flow of assets to terrorist organizations, commercial aviation, the role of congressional oversight and resource allocation, and other areas determined relevant by the Commission. In pursuing our mandate, we have reviewed more than 2.5 million pages of documents and interviewed more than 1,200 individuals in ten countries. This included nearly every senior official from the current and previous administrations who had responsibility for topics covered inour mandate. We have sought to be independent, impartial, thorough, and nonpartisan.
    From the outset, we have been committed to share as much of our investigation as we can with the American people. To that end, we held 19 days of hearings and took public testimony from 160 witnesses.Our aim has not been to assign individual blame. Our aim has been to provide the
    fullest possible account of the events surrounding 9/11 and to identify lessons learned. We learned about an enemy who is sophisticated, patient, disciplined, and lethal. The enemy rallies broad support in the Arab and Muslim world by demanding redress of political grievances, but its hostility toward us and our values is limitless. Its purpose is to rid the world of religious and political pluralism, the plebiscite, and equal rights for women. It makes no distinction between military and civilian targets. Collateral damage is not in its lexicon.We learned that the institutions charged with protecting our borders, civil aviation, and national security did not understand how grave this threat could be, and did not adjust their policies, plans, and practices to deter or defeat it. We learned of fault lines within our government-between foreign and domestic intelligence, and between and within agencies. We learned of the pervasive problems of managing andsharing information across a large and unwieldy government that had been built in a different era to confront different dangers.At the outset of our work, we said we were looking backward in order to look forward. We hope that the terrible losses chronicled in this report can create something positive-an America that is safer, stronger, and wiser. That September day, we came together as a nation. The test before us is to sustain that unity of purpose and meet the challenges now confronting us. We need to design a balanced strategy for the long haul, to attack terrorists and prevent their ranks from swelling while at the same time protecting our country against future attacks. We have been forced to think about the way our government is organized. The massive departments and agencies that prevailed in the great struggles of the twentieth century must worktogether in new ways, so that all the instruments of national power can be combined.Congress needs dramatic change as well to strengthen oversight and focus accountability. As we complete our final report, we want to begin by thanking our fellow Commissioners, whose dedication to this task has been profound. We have reasonedtogether over every page, and the report has benefited from this remarkabledialogue. We want to express our considerable respect for the intellect and judgmentof our colleagues, as well as our great affection for them. We want to thank the Commission staff. The dedicated professional staff, headed by Philip Zelikow, has contributed innumerable hours to the completion of this report,setting aside other important endeavors to take on this all-consuming assignment.They have conducted the exacting investigative work upon which the Commission has built. They have given good advice, and faithfully carried out our guidance. They have been superb. We thank the Congress and the President. Executive branch agencies have searched records and produced a multitude of documents for us. We thank officials, past and present, who were generous with their time and provided us with insight. The PENTTBOM team at the FBI, the Director's Review Group at the CIA, and Inspectors General at the Department of Justice and the CIA provided great assistance. We owe a huge debt to their investigative labors, painstaking attention to detail, and readiness to share what they have learned. We have built on the work of several previous Commissions, and we thank the Congressional Joint Inquiry, whose fine work helped us get started. We thank the City of New York for assistance with documents and witnesses, and the Government Printing Office and W.W. Norton& Company for helping to get this report to the broad public. We conclude this list of thanks by coming full circle: We thank the families of 9/11, whose persistence and dedication helped create the Commission. They have been with us each step of the way, as partners and witnesses. They know better than any of us the importance of the work we have undertaken. We want to note what we have done, and not done. We have endeavored to provide the most complete account we can of the events of September 11, what happened and why.This final report is only a summary of what we have done, citing only a fraction of the sources we have consulted. But in an event of this scale, touching so many issues and organizations, we are conscious of our limits. We have not interviewed every knowledgeable person or found every relevant piece of paper. New information inevitably will come to light. We present this report as a foundation for a better understanding of a landmark in the history of our nation.We have listened to scores of overwhelming personal tragedies and astounding acts of heroism and bravery. We have examined the staggering impact of the events of 9/11 on the American people and their amazing resilience and courage as they fought back. We have admired their determination to do their best to prevent another tragedy while preparing to respond if it becomes necessary. We emerge from this investigation with
     enormous sympathy for the victims and their loved ones, and with enhanced respect
    for the American people. We recognize the formidable challenges that lie ahead.We also approach the task of recommendations with humility. We have made a limited
    number of them. We decided consciously to focus on recommendations we believe to be
    most important, whose implementation can make the greatest difference. We came into this process with strong opinions about what would work. All of us have had to pause, reflect, and sometimes change our minds as we studied these problems and considered the views of others. We hope our report will encourage our fellow citizens to study, reflect-and act.
            Thomas H. Kean, chair
            Lee H. Hamilton, vice chair
    

-  In this example I used ```grep-w``` to print the contents of the Preface.txt file. This is an easy way to access and read the contents of a file. 

# Example 3
#
    rishabhk@RiSHABHK Post_Rate_Comm % find . -mtime -3 
    rishabhk@RiSHABHK Alcohol_Problems % grep -w "depression" *.txt   
    Session2-PDF.txt:other drug use, depression, and anxiety disorders. Many of the
    Session2-PDF.txt:trauma, injuries, assaults,72 depression, and alcohol-related
    Session2-PDF.txt:H. Identification of alcoholism and depression in a geriatric
    Session3-PDF.txt:found effective in the areas of depression, smoking cessation,
    Session4-PDF.txt:of depression: effective disease management strategies to decrease
    

- In this example i used ```grep-w``` and searched the Alcohol_Problems directory for the keyword "depression". This is a useful tool to have as it makes searching for a particular word in hundreds of files easy.
#
# **Command Line Option #2:**  ```grep-l```  
- The ```grep-l``` command allows the user to print out all the files that contain a certain keyword
# Example 1     
    
       rishabhk@RiSHABHK Alcohol_Problems % grep "research" *.txt | wc -l 
       223

- In this example I used ```grep-l and wc-l ``` to find the number of times that the word research was mentioned in the Alcohol_Problems directory. This can be useful for looking through a research to see how many times the author used a particular source.
#   

# Example 2 
     
       
      rishabhk@RiSHABHK Alcohol_Problems % grep -l "" *.txt
       DraftRecom-PDF.txt
       Session2-PDF.txt
       Session3-PDF.txt
       Session4-PDF.txt 
- In this example I printed out all the files in the Alcohol_Problems directory. This is useful to find all the files in certain directory and can be used to find unique files as well.

# Example 3

# 
     rishabhk@RiSHABHK Alcohol_Problems % grep -l "addiction" *.txt
     DraftRecom-PDF.txt
     Session2-PDF.txt
     Session4-PDF.txt  
- In this example I used the ```grep-c``` command filter to find files that went over the topic of addiction. This can be a useful tool to locate all the files that related to certain topic. 
      
