# Resume Analysis Tool

This project provides a tool to evaluate and score resumes based on a given job description (JD). It scores resumes on skill matches, experience, MNC exposure, and educational background, and ranks them to highlight the best candidates.

## Features
- Resume Scoring based on relevant experience and education.
- File Compatibility: Supports PDF, DOCX, and TXT formats.
- RFM Scoring Model for comprehensive evaluation.
- Weighted Composite Score with Similarity Measurement.
- Ranked Output.

## Requirements
- os
- pandas
- sklearn
- PyPDF2
- python-docx
- re
- dash
- dash-bootstrap-components
- plotly

## Installation
1. Clone the repo: `git clone <repo-url>`
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   
## Usage
1.Prepare Data Files:

Place job descriptions in the Dataset/job_descriptions/ directory.
Place resumes in the Dataset/resumes/ directory.
Place reference data files (skill lists, MNCs, institutions) in the ReferenceData/ directory.

2.Run Resume Scoring (project_final_code)

Execute the scoring script to evaluate and rank resumes against the selected job description:
- python project_final_code.py

The results will be saved in cv_scoring_results_new.csv, which includes columns for scores and rankings.

3. Run Dashboard(project_ui_code)
- python project_ui_code.py

## Configuration
1. Paths and Data Files
- Ensure the following files are correctly placed in their respective directories:
           Dataset/job_descriptions/ contains job description files
           Dataset/resumes/ contains resume files.
           ReferenceData/ includes:
               library.txt: List of skills.
               global_skill.txt: Global skills reference.
               tier1.txt: List of MNCs and institutions
               tier2.txt: List of MNCs and institutions
  2. Scoring Parameters:
- You can adjust weights for scoring criteria within the compute_weighted_score() function:
               similarity_weight: Weight for similarity score.
               skill_weight: Weight for skill match score.
               rfm_weight: Weight for RFM score.



