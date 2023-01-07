# discipline_analyses_of_proposals

## Background
It is important for a granting agency to know how the distribution of the applications qua disciplines is. ˆ How many applications belong to Exact Science disciplines, how many fall within one discipline? ˆ How many applications with disciplines outside exact sciences domain have been submitted?

This repository contains code for analyzing the distribution of proposals by discipline. The main objectives are:

1. Determine how many applications belong to Exact Science disciplines and how many fall within other disciplines.

2. Determine how many applications with disciplines outside the exact sciences domain have been submitted.

## Imports

This code imports various modules required for the analysis, including the Tkinter module for importing the submitted proposals file (Example input file submitted proposals.xlsx) and the successful proposals file.

## Data Cleaning

The code turns any NaN values in the dataframes into zero values and checks the excel files in the form of dataframes. It also adds columns for counting the number of discipline appearances per proposal and for counting Exact and Natural sciences (ENW) discipline appearances per proposal.

## Segregating Proposals by Discipline
The code segregates multidiscipline proposals from monodiscipline proposals into separate dataframes, as well as ENW monodiscipline proposals from non-ENW monodiscipline proposals and non-ENW monodiscipline proposals from non-ENW monodiscipline proposals. It also segregates interdomein multidiscipline proposals (those containing ENW disciplines) from intradomein multidiscipline proposals and those without ENW disciplines into separate dataframes.

## Summary Dataframe
The code drops unnecessary columns and creates a summary dataframe. It also creates co-occurrence matrices for submitted and successful proposals, and formats these matrices for use with VOSviewer.

## Finding Disciplines
The code finds the discipline for each monodiscipline proposal and for each intradomein and interdomein multidiscipline proposal. It also finds the disciplines for each monodiscipline successful proposal and for each intradomein and interdomein multidiscipline proposal that was successful in getting a grant.

## Output with Openpyxl
The code uses the openpyxl.utils.dataframe.dataframe_to_rows() function to write a summary of the analysis for monodiscipline, intradomain multidiscipline, and interdomain multidiscipline proposals to subsequent excel sheets. It also writes co-occurrence matrices and files for VOS viewer for submitted and successful proposals, and saves the excel workbook as discipline_analysis.xlsx.

## References
https://stackoverflow.com/questions/74335925/is-there-a-better-way-to-summerize-a-table-information-instead-of-using-iloc-and


















