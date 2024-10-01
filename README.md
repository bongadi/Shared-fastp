# Shared-fastp

# FASTP-Tools

**FASTP Tools** 

**Practical Assignment in preparation for fastp**

Fastp is a powerful and fast tool designed for pre-processing and quality control (QC) of sequencing data, specifically in FASTQ format. It is widely used in bioinformatics for tasks like adapter trimming, quality filtering, and base correction. It is optimized for both speed and ease of use
_____________________________________________________________________________________________________________________________
**Key Functions of fastp:**

1.	**Quality Filtering:**

     o	Per-base quality filtering: fastp can remove low-quality bases from reads, typically those with poor Phred quality scores.

     o	Per-read filtering: fastp filters out entire reads that do not meet a certain quality threshold, ensuring that only high-quality reads are retained for downstream

  	analysis.

3.	**Adapter Trimming:**

  	   o	Automatically detects and trims adapter sequences (short sequences added to each end of the insert as part of the 
         synthesis process) from sequencing reads, a common issue with short-read sequencing data.

  	   o	Can handle common adapters from platforms like Illumina, but you can also specify custom adapter sequences.

5.	**Trimming of Low-Quality Bases:**

      o	fastp can trim low-quality bases from the start and end of reads (default behavior).

  	 0   You can set thresholds for trimming, like a minimum quality score for bases to be retained in the final reads.


7.	**Read Length Control:**
   
      o	Allows the user to filter reads based on their length (e.g., discard too short or too long reads).
  	
      o	Ensures that only reads within a specified length range are kept.

9.	**Poly-G and Poly-X Tail Trimming:**

  	o	fastp can detect and trim poly-G tails (common in Illumina NovaSeq platforms) and poly-X sequences from reads.

11.	**Correction of Base Errors:**

    o	fastp offers options to correct mismatches and errors in overlapping paired-end reads, improving data quality before further analysis.

12.	**N Content Filtering:**

    o	fastp filters out reads with excessive "N" bases (ambiguous bases), ensuring that only high-confidence reads are retained.

13.	**Quality Control Reporting:**
    
    o	Generates a comprehensive quality control (QC) report in both HTML and JSON formats.
   	
    o	The report includes metrics like read quality, adapter content, GC content, length distribution, and quality score distribution.
   	
    o	It provides detailed visual summaries similar to FastQC.

15.	**Paired-end Data Support**:
    
    o	Handles paired-end reads effectively, maintaining the proper relationship between forward and reverse reads even after trimming.
   	
    o	Can correct sequencing errors in overlapping regions of paired-end reads.
   	
17.	**Base Composition Analysis:**
    
    o	fastp can analyze the GC content and base composition of reads, helping to identify biases in the data.
   	
19.	**Fast Performance:**
    
    o	Optimized for speed, making it suitable for handling large datasets from high-throughput sequencing.
   	
    o	Uses multi-threading to process data faster than many traditional QC tools.

    **FASTP Command**

**Why Use fastp command?**

 •	All-in-one solution: fastp combines functions such as trimming, filtering, and error correction, eliminating the need      
      for multiple tools.
	
•    Fast: It performs these tasks efficiently, making it ideal for processing large datasets.

•	User-friendly reports: The generated reports provide detailed insights into the quality and content of your data,

     helping users make informed decisions about their sequencing experiments.


____________________________________________________________________________________________________________________________

1.	**Run wsl to access a **new** terminal**.

    By default, when you install Conda, a base environment is created and often activated unless you deactivate it or switch to another Conda environment. Therefore, you

  	are likely to see that that the base Conda environment is currently active e.g.  (base) 
 
       ![image](https://github.com/user-attachments/assets/2eb36a88-5da4-4836-b302-27177483d069)

2.	**Identify the path to the directory you are currently in by using the command**:  

            pwd
     
 You should be able see the path e.g.    /home/bongadi

     
  ![image](https://github.com/user-attachments/assets/7c74c800-db93-41af-b71c-8f2d445b8034)


3.	**Verify your Conda installation by running the command**:     

  	        	Conda --version 

  	 You should see the installed version of Conda e.g. conda 24.7.1

      ![image](https://github.com/user-attachments/assets/b6e69efc-1458-4857-8d76-3d30c8988667)


5.	**Create a new environment in conda: called fastp**.

            conda create -n fastp
             
    ![image](https://github.com/user-attachments/assets/fdeb768a-bbef-4ed2-81c8-0bfd08495b1c)


6.	**Activate the fastp environment**.
               
               conda activate fastp
            
     ![image](https://github.com/user-attachments/assets/7afede52-2ac3-46b6-8036-4aa507c670ce)

     ![image](https://github.com/user-attachments/assets/6b767b30-c7c7-42e2-ab7b-192f56accc29)


6.	**Install the fastp package from the bioconda channel using Conda**

                conda install -c bioconda fastp
     
     ![image](https://github.com/user-attachments/assets/507451c4-322d-48ae-884e-9e596a551d5d)

 
7.	**Run Fastp command for adaptor trimming**.
          
    ![image](https://github.com/user-attachments/assets/df400f38-450a-4ee0-b064-cdf3285610e4)

    ![image](https://github.com/user-attachments/assets/31f6aa17-87df-4c08-a14c-b68e80a452e4)

8.	**Command for paired reads** 

  	        fastp -i input_R1.fastq -I input_R2.fastq -o output_R1.fastq -O output_R2.fastq

10.	**Generate Quality Reports**:

            fastp -i input.fastq -o output.fastq -h report.html -j report.json

**NOTE:** Fastp is a versatile and efficient tool for cleaning and quality-checking raw sequencing data before further bioinformatics analyses.
     


