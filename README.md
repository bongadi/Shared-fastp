

    

 



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
     


