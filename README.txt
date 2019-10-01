## A new Simple version for Java1.8 is available. Please try it first if you have Java1.8
#the link to it is:
https://github.com/wacguy/Simple-1.8.1

Always use this GitHb README.txt version (and not the Plant Physiology one).

# SIMPLE — A SIMPLE pipeline for mapping point mutations

#####   SYSTEM REQUIREMENTS  #####

# Runs on mac (10.11.6) with X11 and Linux (centOS 6.7)

# Requires Java 1.7 (7u79; http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html)

# Requires R and the following packages: ggplot2, reshape2 and ggrepel
# requires Command Line Tools in Mac OS X

# internet connection

##### RUNNING SIMPLE #####

1. Download and unpack the Simple package from the following link: https://github.com/wacguy/Simple by pressing the green link: "Clone or download"

2. Place the Simple folder in your home directory.

3. Rename your fastq files as follow. For the mutant and WT bulk, the names should start with mut. and wt. respectively (note the dot); for single or paired-end you should then have R1 or R1 and R2, respectively and end with .fastq. For example, if your mutant bulk was sequence in a paired-end format and the WT as single-end you should rename the three files as follow: mut.R1.fastq, mut.R2.fastq and wt.R1.fastq.

4.If you would like to have the name of your output files be specific to the line you are mapping, open the simple_variables.sh file and change the line variable from “EMS” to your line name.  Letters and underscores only, please. This name will be the prefix to all of your output files (this line should look like: line=linename).

5. Place the renamed fastq files in the fastq folder located in the Simple folder.

6. Open the folder scripts inside Simple; open the data_base.txt file. Locate your species in the first column and copy it. 

7. Open the file simple_variables.sh inside the folder scripts with a text editor and paste the species name you've just copied to replace Arabidopsis_thaliana as the species name (e.g., this line should look like: my_species=Arabidopsis_thaliana or my_species=Oryza_sativa_Japonica). save the file.

8. If the mutation you are mapping is dominant, in the simple_variables.sh file, change the mutation from recessive to dominant. This line should look like: mutation=dominant. save the file.

9. Open the Terminal application.

10. Type: cd ~/Simple. Press return.

11. Type: chmod +x ./scripts/simple.sh. Press return.

12. Type: ./scripts/simple.sh. Press return.

13. The last command will execute the program.

14. The script will run for a few hours up to a couple of days, depending on the size of your fastq files and the size of the genome you are working with. You will know it finished once the prompt shows the following colorful text: “Simple is done”.



