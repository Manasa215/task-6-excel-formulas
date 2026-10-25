# Rollback Evidence and Recovery Plan

## Project type
This repository contains a spreadsheet workbook and documentation, not a live application or database. Rollback means restoring the last known-good workbook and repository revision.

## Before changes
1. Keep a copy of the submitted workbook as `Task6_Excel_Formulas_Workbook.xlsx`.
2. Record the commit hash of the known-good version in the GitHub repository history.
3. Check that the workbook opens and the formulas are visible in Excel or Google Sheets.

## Rollback procedure
1. Open the repository's **Commits** history.
2. Select the last known-good commit before the problematic change.
3. Use GitHub's revert option when available, or download the workbook from that commit and replace the broken workbook.
4. Commit the restored workbook with a message such as `Restore last known-good Task 6 workbook`.
5. Reopen the restored workbook and verify a lookup, an IF formula, and the SUMIFS/COUNTIFS examples.

## Evidence to capture after you upload
Save screenshots in this folder (or add them to the repository) if the internship portal requires evidence:
- `github-repository.png`: repository page showing the files and public visibility.
- `workbook-formulas.png`: Excel Formula Practice sheet showing formulas and outputs.
- `commit-history.png`: GitHub commit history showing the original upload and any restore/revert commit.

## Current evidence status
This document describes the rollback procedure and identifies evidence to capture. It does **not** claim that a rollback was executed. Capture real screenshots only after you perform the corresponding GitHub/workbook steps.
