# Week Three

## Regex
 
 - This link gives all the shortcuts in terms of regular expressions (great tool)
   - https://jdhao.github.io/2019/02/28/sublime_text_regex_cheat_sheet/
 
 - Searches for certain word, but highlights the entire line where the word exists
  - .+\bto\b.+
 
 - Insert a character or phrase within the line containe "to'
  - Find: (.+\<to\>)
  - Replace: ~\1
    - this command put a "~" at the beginning of every line
    
 - When deleting all lines without a tilde in front of them
  - Find: \n[^~]+
  - Replace: \n
  
 - After several of these steps, I have compacted 55000 lines from the original text to about 1000 lines desired from the original text
 
 - In this example on the Republic of Texas, for each line that started with a tilde, we wanted to fix the end of the lines where the dates and pages reside. 
 - Find: (,)( [0-9]{4})(.+)
 - Replace: \2
   - This command got rid of the page numbers and just kept the dates (the 2nd part of this series)
   
 - Insert "Sender, Recipient, Date" on a new line 1
 
 - Save document as a csv file
  - When document is saved as a "csv" file, it can opened by the application "Numbers" on Macs
  - When opened on this application, it is organized into the 3 "sender, recipient, date" coloumns


## OpenRefine
 - Had problems at first downloading this program
 - Had to go to the github link then download from there. Make sure OpenRefine is working in your browser
 - Steps include: choosing file, creating project with new name
 
 - Click option "Facet", then 'Text Facet', a box with all the names then appears on the left coloumn
 - Click option "cluster", then play around with the different options available
 - Two names that are supposed to be together but might be seperated due to a little error can be merrged by selecting the 'Merge', then 'Merge Selected and Re Cluster'
 
 - By merging these different inputs, the number of recipients should reduce significantly
 
 - Finishing the cleaning of the data:
   - Edit Cells
   - Common Trasnforms
   - Trim leading and trailing whitespace
   
 - This process had to done for both sender and recipient in this example
   - From there, 'Export' file to return it to a csv file
