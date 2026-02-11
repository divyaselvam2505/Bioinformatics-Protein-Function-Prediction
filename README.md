# Project Title 
In-Silico Identification and Functional Characterization of Target Protein UniProt ID: A0A0H3K5Y8
# Author
Divya S
Msc Bioinformatics
Stella Maris college
Email: divyaselvam@gmail.com
# Description
This repository presents a single continuous bioinformatics pipeline for quality analysis, validation, homology-based functional annotation, and biological interpretation of a protein sequence, predicting thiol methyltransferase activity
#  Project Objective
The objective of this project is to:
•	Retrieve the protein sequence of UniProt ID A0A0H3K5Y8
•	Evaluate its sequence quality and biological validity
•	Apply filtering and validation criteria
•	Identify homologous proteins using BLAST
•	Predict the biological function using homology-based annotation
•	Interpret results in a research-oriented manne
# Single Continuous Pipeline 
This project follows a dependency-based pipeline, where each step depends on the previous one:
1.	Sequence Retrieval
2.	Sequence Quality & Basic Analysis
3.	Sequence Filtering & Validation
4.	Homology Search (BLAST)
5.	Functional Annotation
6.	Biological Interpretation
This mirrors how real bioinformatics research is performed.
# Pipeline 
Step 1: Biological Sequence Selection (Research Setup)
•	Selected sequence: Protein with UniProt ID A0A0H3K5Y8
•	Source: UniProt Knowledgebase (Swiss-Prot/TrEMBL)
•	Format: FASTA
•	The protein was treated as an unknown or poorly characterized sequence for computational analysis.
Why this step exists:
Bioinformatics research always starts with a biological question and a sequence of interest, not with tools.
________________________________________
Step 2: Sequence Quality & Basic Analysis
Using Biopython, the following quality parameters were computed:
•	Protein length
•	Amino acid composition (%)
This analysis ensures the sequence:
•	Has biologically reasonable length
•	Displays valid amino acid distribution
📄 Output file:
results/qc_summary.txt
Why this step exists:
Before trusting any sequence, researchers first confirm that it appears biologically meaningful.
________________________________________
Step 3: Sequence Filtering & Validation (Decision Point)
Biological validation rules were applied:
•	Minimum length threshold: 50 amino acids
•	Ambiguous amino acids checked: X, B, Z, J
Validation result:
•	Sequence passed all criteria
•	Approved for downstream BLAST and annotation
📄 Output file:
results/sequence_validation.txt
Why this step exists:
This step simulates scientific decision-making, not blind execution of commands.
________________________________________
Step 4: Homology Search (BLAST – Core Research Step)
•	Tool used: BLASTp
•	Database: NCBI non-redundant (nr)
•	Input: Protein sequence A0A0H3K5Y8
•	Top homologs identified: Based on E-value, score, and alignment length
📄 Output files:
•	results/blast_results.xml
•	results/blast_results.txt
Why this step is central:
Homology is the foundation of functional prediction.
Proteins with significant sequence similarity often share similar molecular functions.
________________________________________
Step 5: Functional Annotation (Answering the Research Question)
Using the top BLAST hit, the following were extracted:
•	Hit ID and description
•	Alignment length
•	E-value
•	Bit score
•	Percent identity
📄 Output file:
results/functional_annotation.txt
🔍 Predicted Function 
Based on strong sequence similarity to the top BLAST hit, UniProt ID A0A0H3K5Y8 is predicted to:
•	Encode a protein with similar molecular function and biological role as its closest homolog
•	Likely participate in cellular/metabolic processes conserved across related organisms
________________________________________
Step 6: Biological Interpretation (Final Research Outcome)
By integrating:
•	Sequence quality metrics
•	Validation criteria
•	Homology evidence
•	Functional annotation
We conclude that:
Protein A0A0H3K5Y8 is a biologically valid protein with strong homology to known proteins, allowing its molecular function to be predicted using computational methods.
This step transforms the project from an assignment into a research-style analysis.
________________________________________
# Project Structure 
Functional_Sequence_Characterization/
│
├── data/
│   └── A0A0H3K5Y8_sequence.fasta
│
├── analysis/
│   ├── sequence_qc.py
│   ├── sequence_validation.py
│   └── homology_analysis.py
│
├── results/
│   ├── qc_summary.txt
│   ├── sequence_validation.txt
│   ├── blast_results.xml
│   ├── blast_results.txt
│   └── functional_annotation.txt
│
└── README.md
________________________________________
# Tools & Technologies Used
•	Python
•	Biopython
•	BLAST (NCBI)
•	UniProt Knowledgebase
•	FASTA format
________________________________________



