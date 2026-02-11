# Project Title 
In-Silico Identification and Functional Characterization of a Target Protein
UniProt ID: A0A0H3K5Y8
# Author
Divya S
Msc Bioinformatics
Stella Maris college
Email: divyaselvam@gmail.com
# Description
This repository presents a single continuous bioinformatics pipeline for quality analysis, validation, homology-based functional annotation, and biological interpretation of a protein sequence, predicting thiol methyltransferase activity
# Project Overview
This project performs a computational functional characterization of a protein sequence retrieved from the UniProt Knowledgebase (ID: A0A0H3K5Y8).
The workflow follows a structured bioinformatics pipeline:
1.	Sequence Retrieval
2.	Quality Assessment
3.	Validation & Filtering
4.	Homology Search (BLAST)
5.	Functional Annotation
6.	Biological Interpretation
The objective is to predict the molecular function of a poorly characterized protein using homology-based computational methods.
________________________________________
# Biological Data Source
•	Database: UniProt Knowledgebase
•	Sequence ID: A0A0H3K5Y8
•	Format: FASTA
•	Treated as: Unknown / hypothetical protein
________________________________________
# Methodology Pipeline
Step 1 — Sequence Retrieval
The protein sequence was retrieved from UniProt in FASTA format and stored for downstream analysis.
________________________________________
Step 2 — Sequence Quality & Basic Analysis
Using Biopython, the following were computed:
•	Protein length
•	Amino acid composition (%)
•	Biological plausibility check
📄 Output:
results/qc_summary.txt
This ensures the sequence is biologically meaningful before further analysis.
________________________________________
Step 3 — Sequence Filtering & Validation
Validation criteria applied:
•	Minimum length threshold: 50 amino acids
•	Checked for ambiguous residues (X, B, Z, J)
Result:
The sequence passed all validation criteria and was approved for downstream analysis.
📄 Output:
results/sequence_validation.txt
________________________________________
Step 4 — Homology Search (Core Analysis)
Homology search was performed using:
•	Tool: BLASTp
•	Database: National Center for Biotechnology Information (NCBI) non-redundant (nr) database
Top homologs were evaluated based on:
•	E-value
•	Bit score
•	Alignment length
•	Percent identity
📄 Outputs:
results/blast_results.xml
results/blast_results.txt
Homology-based annotation is the foundation for protein function prediction.
________________________________________
Step 5 — Functional Annotation
Using the top BLAST hit, the following were extracted:
•	Hit description
•	Alignment statistics
•	Functional insights
📄 Output:
results/functional_annotation.txt
________________________________________
# Predicted Functional Insight
Based on strong sequence similarity to characterized homologs:
•	The protein likely shares conserved molecular function.
•	It may participate in fundamental cellular or metabolic pathways.
•	Functional prediction is supported by statistically significant BLAST alignment metrics.
This demonstrates how computational biology can infer biological roles without laboratory experimentation.
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
# Tools & Technologies
•	Python
•	Biopython
•	BLASTp
•	UniProt Knowledgebase
•	NCBI nr database
•	FASTA format
________________________________________
# How to Run the Project
1.	Install dependencies:
2.	pip install biopython
3.	Place the FASTA sequence inside the data/ folder.
4.	Run analysis scripts sequentially:
5.	python sequence_qc.py
6.	python sequence_validation.py
7.	python homology_analysis.py
8.	Check the results/ folder for output files.
________________________________________
# Key Learning Outcomes
•	Biological sequence validation before analysis
•	Quality control in computational biology
•	Homology-based functional prediction
•	Research-style pipeline structuring
•	Reproducible bioinformatics workflow
________________________________________
# Research Significance
This project simulates real-world bioinformatics research where:
•	Sequence data is first validated
•	Homology determines functional inference
•	Biological conclusions are derived from computational evidence
It transforms a raw sequence into a biologically interpretable result through systematic analysis.


