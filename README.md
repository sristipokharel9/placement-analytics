# Placement Analytics: What Skills Lead to Better Offers?

## Dataset
1,500 students across 7 departments. Missing values (8 per numeric column) were filled with the median. No duplicates or invalid values were found.

## Key Insights
1. Overall placement rate is 82.8% (1,242 of 1,500).
2. Coding, project and academic scores are the top drivers of placement.
3. Multiple-offer students have higher coding scores (76.2 vs 66.6 for unplaced) and more internships.
4. Coding strongly correlates with salary (r = 0.64); salary rises from 3.81 LPA (<60) to 6.53 LPA (80+).
5. Certifications add value beyond marks: about +0.21 LPA each, and placement rises from 67.6% to 87.8% for low-marks students with 3+ certs.
6. Departments differ little (81% to 86% placement), so skill gaps matter more than department.
7. Communication scores are uniformly high and less differentiating.

## Model
Random Forest Classifier (300 trees, balanced class weights). Target: Placement_Status.
Offer_Count and Salary were excluded to avoid data leakage.
Test ROC-AUC about 0.72. At the default 0.5 cut-off, recall for Not Placed was only 0.02, so the
decision threshold was lowered to [YOUR CHOICE] to catch more at-risk students (recall [X], precision [Y]).
Details: models/metrics.txt

## Action Plan
- Coding practice programme for students below 70
- Certification drive (3+ per student)
- Mandatory projects and at least one internship
- Model-based early-warning list of at-risk students
- College-wide skill programmes rather than department-specific ones

## Visualisations
See the images/ folder.
